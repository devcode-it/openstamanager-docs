---
title: Stampe
sidebar:
  nav: docs-sidebar
---

# stampe

All'interno del gestionale, vengono considerate _stampe_ tutte le strutture che si occupano di generare dei file PDF che l'utente può successivamente visualizzare ed eventualmente salvare/stampare.

Tutte le stampe di OpenSTAManager sono contenute all'interno della cartella `templates/`, raggruppate per nome in un cartelle indipendenti.

La maggior parte delle stampe viene generata attraverso il framework [MPDF](https://github.com/mpdf/mpdf).

## Struttura

Ogni stampa e le caratteristiche di default \(cartella `templates/base/`\) sono personalizzabili con la relativa cartella `custom/`, come documentato nella sezione [Codice](../base/code.md).

Il sistema di template delle stampe presenta una gestione automatica per la sostituzione di alcune variabili comuni:

* `$default_header$`: contenuti dell'header di default
* `$default_footer$`: contenuti del footer di default
* `$default_logo$`: percorso del logo di default
  * percorso dall'impostazione **Logo stampe**
  * `templates/base/logo_azienda.jpg`
* `$logo$`: percorso del logo della stampa \(`logo_azienda.jpg` nella cartella della stampa, oppure $default\_logo$\)
* `$docroot$`: DOCROOT
* `$rootdir$`: ROOTDIR
* `$directory$`: percorso della stampa
* `$footer$`: footer aggiuntivo personalizzato
* `$dicitura_fissa_fattura$`: **Dicitura fissa fattura** dalle **Impostazioni**

Sono inoltre disponibili attraverso il formato `$c_*$` tutte le informazioni dell'anagrafica cliente e sotto `$f_*$` tutte le informazioni dell'anagrafica azienda.

### settings.php

Il file `settings.php` permette di gestire le seguenti impostazioni PDF della stampa:

```php
<?php

return [
    'orientation' => 'P', // Orientamento: P (verticale) o L (orizzontale)
    'format' => 'A4', // Formato della pagina
    'font-size' => 10, // Dimensione dei font
    'margins' => [
        'top' => 10, // Margine superiore
        'bottom' => 10, // Margine inferiore
        'left' => 12, // Margine sinistro
        'right' => 12, // Margine destro
    ],
    'header-height' => 35, // Altezza dell'header (da modificare se personalizzato)
    'footer-height' => 5, // Altezza del footer (da modificare se personalizzato)
];
```

Le impostazioni di default sono presenti nel file `templates/base/settings.php`.

### init.php

Il file `init.php` si occupa di definire le variabili principali necessarie per il corpo della stampa. Idealmente, questo file si occupa di gestire tutte le interazioni della stampa con le altre strutture del gestionale e del database.

Ci sono, in particolare, 3 variabili particolarmente importanti:

* `$id_cliente`: individua il cliente interessato dalla stampa \(per rendere disponibili le variabili `$c_*$`\)
* `$id_sede`: individua la sede relativa del cliente
* `$custom`: array per definire i valori personalizzati da sostituire nel template

  ```php
  // Sostituzioni specifiche
  $custom = [
  'intervento_numero' => $records[0]['codice'],
  'intervento_data' => Translator::dateToLocale($records[0]['data_richiesta']),
  'commessa_numero' => !empty($records[0]['numero_preventivo']) ? $records[0]['codice'] : '&nbsp;',
  ];
  // Rende disponibili le variabili aggiuntive: $intervento_numero$, $intervento_data$, $commessa_numero$.
  ```

### body.php

Il file `body.php` gestisce tutti i contenuti principali della stampa PDF, eventualmente suddividendoli in varie pagine. Ogni stampa può gestire liberamente il proprio codice in questa sezione.

Se si desidera sfruttare la funzione di auto-riempimento approssimativo delle tabelle, è necessario definire le impostazioni relative:

```php
$autofill = [
    'count' => 0, // Conteggio delle righe
    'words' => 70, // Numero di parolo dopo cui contare una riga nuova
    'rows' => 20, // Numero di righe massimo presente nella pagina
    'additional' => 15, // Numero di righe massimo da aggiungere
    'columns' => 5, // Numero di colonne della tabella
];
```

Ogni volta che viene aggiunta manualmente una riga, è necessario aumentare di conseguenza il valore di `$autofill['count']` per permettere il corretto funzionamento del sistema.

### header.php

Il file `header.php` si occupa della generazione dell'header di ogni pagina del PDF, in modo da avere una struttura comune di base. La sua presenza è facoltativa, nel qual caso viene utilizzato l'header di default.

Il logo della stampa deve essere sempre inserito con il seguente codice:

```markup
<img src="$logo$" alt="Logo" border="0"/>
```

L'header di default è presente nel file `templates/base/header.php`.

### footer.php

Il file `footer.php` si occupa della generazione del footer di ogni pagina del PDF, in modo da avere una struttura comune di base. La sua presenza è facoltativa, nel qual caso viene utilizzato il footer di default.

Il footer di default è presente nel file `templates/base/footer.php`.

## Problemi

### Testo piccolo nelle tabelle

Come indicato nel secondo punto in [http://mpdf.github.io/tables/auto-layout-algorithm.html](http://mpdf.github.io/tables/auto-layout-algorithm.html), MPDF effettua un resizing del font nel caso il contenuto di una cella superi l'altezza totale di una pagina. Si possono quindi verificare dei problemi con le dimensioni del testo nel caso ci siano contenuti molto lunghi.

Pertanto, nel caso si desideri aumentare le dimensioni del font, si consiglia di effettuare alcuni test per controllare se le tabelle vengono renderizzate nel modo corretto e previsto.

## HTML2PDF

Il formato delle stampe più vecchie viene strutturato per la generazione attraverso il framework [HTML2PDF](https://github.com/spipu/html2pdf).

### Struttura

#### pdfgen.php

Il file `pdfgen.php` si occupa della formattazione dei contenuti dei template per la visualizzazione vera e propria del PDF, inizializzando l'oggetto relativo ed eseguendone l'output.

#### pdfgen\_variables.php

Il file `pdfgen_variables.php` si occupa della sostituzione delle variabili comuni a tutti i template, e viene richiamata dal file `pdfgen.MODULO.php` descritto di seguito.

#### Struttura interna

La cartella _templates_ contiene tutti i template per la creazione dei PDF relativi al modulo specifico, in una struttura interna simile alla seguente \(modulo **Contratti** utilizzato come esempio\).

```text
.
└── contratti
    ├── contratto_body.html - Struttura di base del PDF
    ├── contratto.html - Contenitore personalizzato della struttura del PDF
    ├── logo_azienda.jpg - Logo dell'azienda specifico per il PDF
    └── pdfgen.contratti.php - Individuazione delle informazioni da visualizzare e generazione della loro struttura
```

