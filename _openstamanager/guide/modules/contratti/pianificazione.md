---
title: Plugin Pianificazione attività
add:
  - path: add-alert.png
    alt: Messaggio informativo
    title: Messaggio informativo per la creazione del promemoria
  - path: add.png
    alt: Schermata di creazione (concluso)
    title: Schermata di creazione del promemoria
  - path: add-data.png
    alt: Schermata di creazione (completa)
    title: Schermata di creazione del promemoria compilata
---

# pianificazione

Il plugin **Pianificazione attività** è una componente del modulo **Contratti** dedicata alla completa gestione della pianificazione delle attività \(_promemoria_\) relative ai contratti registrati all'interno di OpenSTAManager.

## Navigazione

Il plugin è raggiungibile, all'interno dell'area di modifica di un _record_ del modulo **Contratti**, attraverso il menu dedicato nella sezione alta a destra della schermata, sotto la dicitura **Pianificazione attività**.

## Caratteristiche

La schermata principale del plugin è strutturata secondo una tabella personalizzata, sotto alcune istruzioni di base sull'utilizzo del plugin.

La possibilità di creare nuovi elementi viene resa disponibile dal pulsante _Nuovo promemoria_ \(che apre una struttura grafiche, _modal_, sovrapposta agli altri contenuti\), ma **non è possibile modificare un promemoria pre-esistente**.

### Creazione

Come descritto sopra, la creaazione di nuovi elementi viene resa disponibile dal pulsante _Nuovo promemoria_. Una volta cliccato il pulsate, verrà aperto un messaggio informativo con la richiesta di selezionare la tipologia di attività relativa al nuovo promemoria; successivamente verrà visualizzata un _modal_ con la possibilità di completare le informazioni dell'elemento.

Ogni promemoria può possedere articoli, spese generiche e allegati indipendenti, oltre ai campi:

* Data del promemoria
* Sede
* Impianti interessati
* Descrizione

### Pianificazione ciclica

Una volta creato il promemoria, sarà possibile effettuare una pianificazione ciclica dello stesso attraverso seguente pulsante della relativa riga.

In fondo al _modal_ di riepilogo che compare dopo il click sul pulsante relativo, saranno visibili nuovi due raggruppamenti:

* _Promemoria ciclico?_
* _Pianificare interventi?_ per rendere automaticamente il promemoria un'attività

La pianificazione di promemoria ciclici replicherà in modo completo le caratteristiche del promemoria selezionato \(compresi articoli, spese generiche e allegati\), aggiornando le date di conseguenza.

### Trasformazione in attività

Una volta creato il promemoria, sarà possibile trasformarlo in attività in modo indipendete dalla funzione di [_Pianificazione ciclica_](pianificazione.md#pianificazione-ciclica) attraverso il pulsante dedicato nella relativa riga.

Questa azione permetterà quindi di confrontarsi con la classica schermata per la creazione delle attività, pre-impostata secondo le caratteristiche del promemoria.

## Particolarità

I promemoria verranno successivamente visualizzati nel modulo **Dashboard** per semplificare la pianificazione del giorno dell'intervento, ad esempio nel caso di interventi con cadenza mensile.

