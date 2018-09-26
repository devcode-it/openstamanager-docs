---
title: Plugin Pianificazione attività
add:
  - path: add-alert.png
    alt: "Messaggio informativo"
    title: "Messaggio informativo per la creazione del promemoria"
  - path: add.png
    alt: "Schermata di creazione (concluso)"
    title: "Schermata di creazione del promemoria"
  - path: add-data.png
    alt: "Schermata di creazione (completa)"
    title: "Schermata di creazione del promemoria compilata"
---

Il plugin **Pianificazione attività** è una componente del modulo **Contratti** dedicata alla completa gestione della pianificazione delle attività (*promemoria*) relative ai contratti registrati all'interno di OpenSTAManager.

## Navigazione

Il plugin è raggiungibile, all'interno dell'area di modifica di un *record* del modulo **Contratti**, attraverso il menu dedicato nella sezione alta a destra della schermata, sotto la dicitura **Pianificazione attività**.

## Caratteristiche

La schermata principale del plugin è strutturata secondo una tabella personalizzata, sotto alcune istruzioni di base sull'utilizzo del plugin.

La possibilità di creare nuovi elementi viene resa disponibile dal pulsante *Nuovo promemoria* (che apre una struttura grafiche, *modal*, sovrapposta agli altri contenuti), ma **non è possibile modificare un promemoria pre-esistente**.

{% include figure path="controller.png" alt="Plugin Pianificazione attività" caption="Screenshot del plugin **Pianificazione attività**" %}

### Creazione

Come descritto sopra, la creaazione di nuovi elementi viene resa disponibile dal pulsante *Nuovo promemoria*.
Una volta cliccato il pulsate, verrà aperto un messaggio informativo con la richiesta di selezionare la tipologia di attività relativa al nuovo promemoria; successivamente verrà visualizzata un *modal* con la possibilità di completare le informazioni dell'elemento.

{% include gallery id="add" caption="Schermate di creazione" %}

Ogni promemoria può possedere articoli, spese generiche e allegati indipendenti, oltre ai campi:
 - Data del promemoria
 - Sede
 - Impianti interessati
 - Descrizione

{% include figure path="row-list.png" alt="Promemoria creato" caption="Screenshot del plugin con promemoria" %}

### Pianificazione ciclica

Una volta creato il promemoria, sarà possibile effettuare una pianificazione ciclica dello stesso attraverso seguente pulsante della relativa riga.

{% include figure path="options-pianifica.png" alt="Opzione di pianificazione" caption="Screenshot dell'opzione di pianificazione" %}

In fondo al *modal* di riepilogo che compare dopo il click sul pulsante relativo, saranno visibili nuovi due raggruppamenti:
 - *Promemoria ciclico?*
 - *Pianificare interventi?* per rendere automaticamente il promemoria un'attività

{% include figure path="pianifica-ciclo.png" alt="Pianificazione ciclica" caption="Screenshot della sezione di pianificazione ciclica" %}

{% include figure path="pianifica-intervento.png" alt="Pianificazione intervento" caption="Screenshot della sezione di pianificazione intervento" %}

La pianificazione di promemoria ciclici replicherà in modo completo le caratteristiche del promemoria selezionato (compresi articoli, spese generiche e allegati), aggiornando le date di conseguenza.

{% include figure path="row-list-final.png" alt="Pianificazione intervento" caption="Screenshot della sezione di pianificazione intervento" %}

### Trasformazione in attività

Una volta creato il promemoria, sarà possibile trasformarlo in attività in modo indipendete dalla funzione di [*Pianificazione ciclica*](#pianificazione-ciclica) attraverso il pulsante dedicato nella relativa riga.

{% include figure path="options-intervento.png" alt="Opzione di pianificazione" caption="Screenshot dell'opzione di pianificazione" %}

Questa azione permetterà quindi di confrontarsi con la classica schermata per la creazione delle attività, pre-impostata secondo le caratteristiche del promemoria.

{% include figure path="add-intervento.png" alt="Creazione attività da promemoria" caption="Screenshot della schermata di creazione attività da promemoria" %}

## Particolarità

I promemoria verranno successivamente visualizzati nel modulo **Dashboard**  per semplificare la pianificazione del giorno dell'intervento, ad esempio nel caso di interventi con cadenza mensile.

{% include figure path="more.png" alt="Pianificazione attività in Dashboard" caption="Screenshot della **Dashboard** con promemoria" %}
