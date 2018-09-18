---
title: Modifica attività
sign:
  - path: sign-form.png
    alt: "Anteprima del PDF"
    title: "Anteprima del PDF"
  - path: sign.png
    alt: "Schermata di firma"
    title: "Schermata di firma"
info:
  - path: sign-none.png
    alt: "Firma mancanteF"
    title: "Firma mancante"
  - path: sign-ok.png
    alt: "Firma effettuata"
    title: "Firma effettuata"
---

La sezione di modifica degli elementi del modulo segue il sistema standard del gestionale, necessitando il click sulla riga relativa al *record* all'interno della tabella della schermata principale.

## Caratteristiche

Una volta all'interno di questa parte del sistema, il modulo **Attività** permette di completare *tutte* le informazioni che il gestionale supporta per le attività.
In particolare, per permettere un maggiore senso logico nella navigazione dei dati, la sezione di modifica è suddivisa in vari raggruppamenti.

### Dati cliente

Il primo raggruppamento di informazioni consiste nell'insieme dei dati relativi al cliente selezionato.

{% include figure path="section-1.png" alt="Dati cliente" caption="Screenshot della sezione dei dati cliente" %}

Attraverso questa sezione, è possibile procedere alla modifica di alcune informazioni di base:
 - Cliente dell'attività
 - Sede di esecuzione attività
 - Cliente per conto di cui viene eseguita l'attività
 - Referente di contatto
 - Preventivo collegato
 - Contratto collegato

Per maggiori informazioni sulla relazine dell'attività con [**Preventivi**](../../preventivi.md) e [**Contratti**](../../contratti.md), visitare le sezioni relative.

### Dati intervento

Viene quindi presentata una selezione di campi relativi alle informazioni dell'attività stessa, quali:
 - Data di richiesta
 - Zona relativa
 - Tipo di attivitò
 - Stato dell'attività
 - Eventuale automezzo utilizzato
 - Richiesta
 - Descrizione
 - Note interne

{% include figure path="section-2.png" alt="Dati intervento" caption="Screenshot della sezione dei dati intervento" %}

### Spese e costi

Esiste quindi una macro-sezione dedicata alla gestione dei costi relativi all'attività, suddivisi in particolare in tre categorie:
 - Ore di lavoro dei tecnici
 - Materiali utilizzati
 - Spese ulteriori

{% include figure path="section-3.png" alt="Spese e costi" caption="Screenshot della macro-sezione di spese e costi" %}

Per maggiori informazioni sulla gestione di queste informazioni, visitare la [sezione dedicata](costi.md).

### Tabella dei costi totali



{% include figure path="section-4.png" alt="Informazioni aggiuntive" caption="Screenshot della sezione di informazioni aggiuntive" %}

## Opzioni

Nella parte superiore della pagina viene inoltre permessa la visualizzazione di una serie di opzioni dedicate al modulo **Attività**:
 - Stampa dell'attività
 - Invio del rapportino via email
 - Visualizzazione dell'anteprima della stampa e [firma conclusiva dell'attività](#anteprima-e-firma)

{% include figure path="options.png" alt="Opzioni" caption="Screenshot della opzioni dell'attività" %}

### Anteprima e firma

La funzionalità di *Anteprima e firma* permette al cliente di firmare l'attività per segnalare l'avvenuto completamento dei lavori.
Una volta firmata l'attività, risulterà impossibile modificarla.

{% include gallery id="sign" caption="Schermate di anteprima e firma" %}

Le infomazioni relative allo stato di firma dell'attività sono visibili in fondo alla pagina dell'attività, nei seguenti formati:
{% include gallery id="info" caption="Informazioni sulla firma" %}
