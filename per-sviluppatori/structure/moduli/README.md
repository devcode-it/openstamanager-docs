---
description: Guida alla struttura dei moduli in OpenSTAManager
---

# 📒 Moduli

> Un modulo (software) è un componente software autonomo e ben identificato, e quindi facilmente riusabile.
>
> [Wikipedia](https://it.wikipedia.org/wiki/Modulo#Informatica)

All'interno del progetto, i moduli vengono genericamente definiti quali sistemi di gestione delle funzionalità del gestionale; proprio per questo, la loro struttura e composizione risulta spesso variabile e differenziata.

Ogni modulo è composto da diverse sezioni, generalmente suddivise in:

* [Nucleo](https://github.com/devcode-it/openstamanager-docs/blob/master/contribuire/structure/broken-reference/README.md);
* [Stampe](stampe.md);
* [Widget](https://github.com/devcode-it/openstamanager-docs/blob/master/contribuire/structure/broken-reference/README.md);
* [Plugin](plugin.md).

OpenSTAManager presenta inoltre una struttura nativamente predisposta alla personalizzazione delle funzioni principali, il che rende il progetto ancora più complicato da comprendere a prima vista.

Di seguito viene presentate le strutture principali più comuni supportate dal gestionale; per ulteriori approfondimenti, si consiglia di controllare il codice sorgente dei moduli ufficiali.

## Struttura

Il codice sorgente di ogni modulo di OpenSTAManager è all'interno di un percorso univoco all'interno della cartella **modules**.

```
.
└── modules
    └── {modulo}
       └── ajax
          ├── complete.php
          ├── search.php
          └── select.php
       └── modals
          └── {modal}.php
       └── plugins
          └── {plugin}.php
       └── src
          └── {object}.php
       ├── actions.php
       ├── add.php
       ├── bulk.php
       ├── buttons.php
       ├── controller_after.php
       ├── controller_before.php
       ├── edit.php
       ├── init.php
       ├── modutil.php
       ├── validation.php
       └── variables.php
       
Il nome dei file contenenti le parentesi graffe {} possono assumere qualsiasi valore.
```

Il gestionale supporta in modo nativo questa struttura, che può essere ampliata e personalizzata secondo le proprie necessità: si consiglia pertanto di analizzare i moduli **Iva**, **Dashboard** e **Contratti** per esempi di diversa complessità.

{% hint style="warning" %}
**Attenzione**: la presenza dei file sopra indicati è necessaria esclusivamente per i _moduli fisici_, cioè moduli che presentano la necessità di interagire con il codice sorgente e modificare i dati del gestionale. Per moduli presenti esclusivamente a livello di database (per sempio, **Movimenti**), si veda la sezione [Database](./#database).
{% endhint %}

### ajax/complete.php

Il file `ajax/complete.php` contiene diversi template HTML che fanno riferimento al modulo e sono gestiti tramite  il parametro `op` che permette di identificare quale template viene richiesto.

Questi template possono essere richiamati da qualsiasi file anche al di fuori del modulo corrispondente.

### ajax/search.php

Il file `ajax/search.php` si occupa di estrarre le informazioni necessarie per la ricerca globale del modulo di riferimento.

Questo avviene tramite l'esecuzione di una query e la visualizzazione in HTML dei risultati ottenuti.

### ajax/select.php

l file `ajax/select.php` contiene le query che fanno riferimento al modulo per quanto riguarda la valorizzazione dei campi input select (menù a tendina), sono gestiti tramite  il parametro `ajax-source` che permette di identificare quale query viene richiesta.

Queste query possono essere richiamate via ajax tramite valorizzando nel campo input l'attributo `ajax-source` da qualsiasi file anche al di fuori del modulo corrispondente.

### modals/{modal}.php

l file `modals/{modal}.php` contiene il template HTML dedicato alla visualizzazione di una specifica pop-up richiamata nel modulo.

### plugins/{plugins}.php

l file `plugins/{plugin}.php` contiene lo script per la gestione di un plugin del modulo di riferimento, in caso di un plugin articolato in più file è necessario utilizzare il percorso `plugins/` specifico.

### src/{object}.php

l file `src/{object}.php` permette la gestione e la creazione di oggetti Eloquent del modulo andando a definire le varie funzioni specifiche dell'oggetto.

### actions.php

Il file `actions.php` gestisce tutte le operazioni supportate dal modulo.

In generale, le diverse operazioni vengono gestite attraverso attraverso una logica basata su casi (solitamente, il parametro `op` permette di identificare quale azione viene richiesta); il funzionamento a livello di programmazione può essere comunque sottoposto a scelte personali.

L'unico requisito effettivo risulta relativo alle operazioni di creazione dei nuovi _record_, per cui deve essere definito all'interno della variabile `$id_record` l'identificativo del nuovo elemento. Per osservare questo sistema, si consiglia di analizzare il relativo file del modulo **Iva**.

### add.php e edit.php

Il file `add.php` contiene il template HTML dedicato all'inserimento di nuovi elementi per il modulo, mentre `edit.php` contiene il template HTML dedicato alla modifica degli stessi.

In base alla configurazione del modulo nel database, il file `edit.php` può assumere il ruolo di gestore della sezione principale dell'interno modulo. Esempi di questa gestione si possono osservare nei moduli **Dashboard** e **Gestione componenti** (si veda la sezione zz\_modules).

**Attenzione**: il progetto individua in automatico la presenza del file `add.php` e agisce di conseguenza per permettere o meno l'inserimento di nuovi _record_. {: .notice--danger}

### bulk.php

Il file `bulk.php` si occupa di gestire le **azioni di gruppo** accessibili nel modulo che vengono visualizzate sotto alla tabella principale.

Il file è formato da due parti, la prima contiene le operazioni di gruppo che vengono effettuate, sempre gestite dal parametro `op`, mentre la seconda parte contiene il template per la visualizzazione all'interno del modulo.

### buttons.php

Il file `buttons.php` viene incluso nel file `edit.php` e viene utilizzato per mostrare nella parte superiore della schermata (in fase di modifica record) i pulsanti/avvisi definiti nel file.

### init.php

Il file `init.php` si occupa di individuare le informazioni principali utili all'identificazione e alla modifica dei singoli elementi del modulo.

In particolare, questo file è solitamente composto da una query dedicata ad ottenere tutti i dati dell'elemento nella variabile `$record` (`$records` per versioni <= 2.4.1), successivamente utilizzata dal gestore dei template per completare le informazioni degli input.

### controller\_after.php e controller\_before.php

Il file `controller_before.php` contiene il template HTML da aggiungere all'inizio della pagina principale del modulo se questo è strutturato in modo tabellare.

Similmente, il file `controller_after.php` contiene il template HTML da aggiungere alla fine della pagina principale nelle stesse condizioni.

### modutil.php

Il file `modutil.php` viene utilizzato per definire le funzioni PHP specifiche del modulo, e permettere in questo modo una gestione semplificata delle operazioni più comuni.

Si noti che un modulo non è necessariamente limitato all'utilizzo del proprio file `modutil.php`: come avviene per esempio in **Fatture** e **Interventi**, risulta possibile richiamare file di questa tipologia da altri moduli (in questo caso, da **Articoli** per la gestione delle movimentazioni di magazzino).

### validation.php

Il file `validation.php` viene utilizzato per effettuare controlli di validazione su un specifico campo input.

Per richiamare la validazione è necessario inserire l'attributo `validation` nel campo input con il nome del controllo da effettuare.

### variables.php

Il file `variables.php` contiene le variabili che possono essere utilizzate nei template delle email per la sostituzione automatica in base al record del modulo.

## Database

All'interno del database del progetto, le tabelle con il suffisso `zz` sono generalmente dedicate alla gestione delle funzioni di base del gestionale.

La gestione dei moduli avviene in questo senso grazie alle seguenti tabelle:

* `zz_modules`;
* `zz_permissions`;
* `zz_views`;
* `zz_plugins`;
* `zz_widgets`.

### zz\_modules

La tabella `zz_modules` contiene tutte le informazioni dei diversi moduli installati nel gestionale in uso, con particolare riferimento a:

* Nome (utilizzato a livello di codice) \[`name`]
* Titolo (nome visibile e personalizzabile) \[`title`]
* Percorso nel file system (partendo da `modules/`) \[`directory`]
* Icona \[`icon`]
* Posizione nella sidebar \[`order`]
* Compatibilità \[`compatibility`]
* Query di default \[`options`]
* Query personalizzata \[`options2`]

Gli ultimi due attributi si rivelano di fondamentale importanza per garantire il corretto funzionamento del modulo, poiché descrivono il comportamento dello stesso per la generazione della schermata principale nativa in OpenSTAManager.

Sono permessi i seguenti valori:

* custom \[Modulo con schermata principale personalizzata e definita nel file `edit.php`]
* {VUOTO} \[Menu non navigabile]
* menu \[Menu non navigabile]
* Oggetto JSON

```javascript
    { "main_query": [ { "type": "table", "fields": "Nome, Descrizione", "query": "SELECT `id`, `nome` AS `Nome`, `descrizione` AS `Descrizione` FROM `tabella` WHERE 2=2 HAVING 1=1 ORDER BY `nome`"} ]}
```

* Query SQL \[vedasi la tabella [zz\_views](./#zz_views-e-zz_group_view)]

```sql
    SELECT |select| FROM `tabella` WHERE 2=2 HAVING 1=1
```

### zz\_permissions e zz\_group\_module

La tabella `zz_permissions` contiene i permessi di accesso dei vari gruppi ai diversi moduli, mentre la tabella `zz_group_module` contiene le clausole SQL per eventualmente restringere questo accesso.

### zz\_views e zz\_group\_view

Le tabelle `zz_views` e `zz_group_view` vengono utilizzate dal gestionale per la visualizzazione delle informazioni secondo i permessi accordati, oltre che dal modulo **Viste** per la gestione dinamica delle query.

### zz\_plugins e zz\_widgets

La tabella `zz_plugins` contiene l'elenco di plugins relativi ai diversi moduli, mentre la tabella `zz_widgets` contiene l'elenco di widgets dei vari moduli.

## Consigli per lo sviluppo

Alla base dello sviluppo di ogni modulo vi è una fase di analisi indirizzata all'individuazione dettagliata delle funzionalità dello stesso e della struttura interna al database atta a sostenere queste funzioni.

Siete dunque pregati di identificare chiaramente tutte le caratteristiche del Vostro nuovo modulo o delle Vostre modifiche prima di iniziare lo sviluppo vero e proprio (comunemente identificato con la scrittura del codice).

> E' bene trascurare le fasi di analisi e di progetto e precipitarsi all'implementazione allo scopo di guadagnare il tempo necessario per rimediare agli errori commessi per aver trascurato la fase di analisi e di progetto.
>
> Legge di Mayers

### Sviluppo

Lo sviluppo del codice deve seguire alcune direttive generali per la corretta interpretazione del codice all'interno del gestionale: ciò comporta una struttura di base fondata sui file precedentemente indicati nella sezione [Struttura](./#struttura) ma ampliabile liberamente.

### Test

Prima di pubblicare un modulo si consiglia di effettuare svariati test in varie installazioni. Siete inoltre pregati di indicare i bug noti.

> Se c’è una remota possibilità che qualcosa vada male, sicuramente ciò accadrà e produrrà il massimo danno.
>
> Legge di Murphy

## Installazione

L'installazione di un modulo è completabile in modo automatico seguendo la seguente procedura:

* Scaricare l'archivio `.zip` del modulo da installare;
* Accedere al proprio gestionale con un account abilita all'accesso del modulo **Aggiornamenti**;
* Selezionare l'archivio scaricato nella selezione file della sezione "Carica un nuovo modulo";
* Cliccare il pulsante "Carica".

Si ricorda che per effettuare l'installazione è necessaria la presenza dell'estensione `php_zip` (per ulteriori informazioni guardare [qui](https://www.php.net/manual/en/zip.installation.php)).

{% hint style="warning" %}
**Attenzione**: la procedura può essere completata anche a livello manuale, ma si consiglia di evitare tale sistema a meno che non si conosca approfonditamente il procedimento di installazione gestito da OpenSTAManager.
{% endhint %}

### Archivio ZIP

L'archivio del modulo deve essere organizzato secondo la seguente struttura:

```
modulo.zip
├── update
|   ├── VERSIONE.sql
|   └── unistall.php
├── ... - File contententi il codice del modulo
└── MODULE
```

Alcuni esempi sulla struttura dei moduli personalizzati sono disponibili nella repository [https://github.com/devcode-it/example](https://github.com/devcode-it/example).

#### update/VERSIONE.sql

Il file `VERSIONE.sql` (dove VERSIONE sta per la versione del modulo con `_`\[underscore] al posto di `.`\[punto]) contiene le operazioni di installazione e aggiornamento del modulo a livello del database, comprendenti la creazione delle tabelle di base del modulo e l'inserimento di ulteriori dati nelle altre tabelle.

#### update/unistall.php

Il file `unistall.php` contiene le operazioni di disinstallazione del modulo a livello del database, e deve prevedere l'eliminazione delle tabelle non più necessarie e dei dati inutilizzati.

```php
<?php

include_once __DIR__.'/../../core.php';

$dbo->query("DROP TABLE `tabella`");
```

#### MODULE

Il file `MODULE` è infine il diretto responsabile dell'installazione del modulo poiché definisce tutti i valori caratteristici dello stesso; in caso di sua assenza la cartella compressa viene considerata non corretta.

```
name = "Nome del modulo"
version = "Versione"
directory = "Cartella di installazione"
options = "Operazione da eseguire all'apertura"
compatibility = "Versioni di compatibilità"
compatibility = "Compatibilità del modulo"
parent = "Genitore del modulo"
```

## Moduli di base

Nella versione base del gestionale sono presenti, all'interno della cartella **modules**, i seguenti moduli.

```
.
├── adattatori_archiviazione
├── aggiornamenti
├── ammortamenti
├── anagrafiche
├── articoli
├── attributi_combinazioni
├── automezzi
├── backups
├── banche
├── beni
├── categorie
├── categorie_contratti
├── categorie_documenti
├── categorie_files
├── causali
├── causali_movimenti
├── checklists
├── combinazioni_articoli
├── contratti
├── custom_fields
├── dashboard
├── ddt
├── descrizioni_predefinite
├── emails
├── eventi
├── fasce_orarie
├── fatture
├── gestione_documentale
├── gestione_task
├── giacenze_sedi
├── impianti
├── import
├── impostazioni
├── interventi
├── iva
├── liste_newsletter
├── listini
├── listini_cliente
├── mansioni
├── mappa
├── marche
├── misure
├── modelli_primanota
├── movimenti
├── newsletter
├── oauth
├── ordini
├── otp_tokens
├── pagamenti
├── partitario
├── piano_sconto
├── porti
├── preventivi
├── primanota
├── provenienza
├── relazioni_anagrafiche
├── ritenute
├── ritenute_contributi
├── rivalse
├── scadenzario
├── segmenti
├── settori_merceologici
├── smtp
├── spedizioni
├── stampe
├── stampe_contabili
├── stati_contratto
├── stati_ddt
├── stati_fattura
├── stati_intervento
├── stati_ordine
├── stati_preventivo
├── statistiche
├── stato_email
├── stato_servizi
├── tags
├── tecnici_tariffe
├── tipi_anagrafiche
├── tipi_documento
├── tipi_intervento
├── tipi_scadenze
├── utenti
├── viste
└── zone
```
