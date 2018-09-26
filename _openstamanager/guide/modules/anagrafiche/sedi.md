---
title: Plugin Sedi
---

Il plugin **Sedi** è una componente del modulo **Anagrafiche** dedicata alla completa gestione di tutte le eventuali sedi delle anagrafiche registrate all'interno di OpenSTAManager.

## Navigazione

Il plugin è raggiungibile, all'interno dell'area di modifica di un *record* del modulo **Anagrafiche**, attraverso il menu dedicato nella sezione alta a destra della schermata, sotto la dicitura **Sedi**.

## Caratteristiche

La schermata principale del plugin è strutturata secondo la tabella generale predefinita, presentando inoltre la possibilità di creare e modificare gli elementi attraverso strutture grafiche che si sovrappongono agli altri contenuti (*modal*).

{% include figure path="controller.png" alt="Plugin Sedi" caption="Screenshot del plugin **Sedi**" %}

### Creazione

La creazione di nuovi elementi segue il funzionamento standard del gestionale, necessitando il click sul pulsante apposito all'interno dell'intestazione del plugin.

{% include figure path="add.png" alt="Creazione sede" caption="Schermata di creazione di una nuova sede" %}

Viene quindi reso possibile compilare tutte le informazioni di base relative alla nuova sede da creare:
 - Nome personalizzato
 - Indirizzo
 - Città
 - CAP
 - Provincia
 - Cellulare
 - Telefono
 - Indirizzo email
 - Zona (per maggiori informazioni, visitare la documentazione del modulo [**Zone**](zone.md))

### Modifica

La schermata di modifica, sebbene molto simile a quella di creazione, permette in particolare di impostare altre informazioni secondarie.

{% include figure path="edit.png" alt="Modifica sede" caption="Schermata di modifica di una sede" %}

E' inoltre possibile indicare un numero predefinito di chilometri (sotto il campo **Distanza/Km**) da riportare su eventuali **Attività** create per l'anagrafica con la sede relativa.

In particolare, se l'impostazione **Google Maps API key** viene impostata, sarà possibile visualizzare attraverso Google Maps l'indirizzo indicato ed eventualmente definire manualmente longitudine e latitudine.

## Particolarità

La sede legale, predefinita per l'anagrafica, non viene registrata allo stesso modo delle altre sedi.
Sarà pertanto impossibile eliminare completamente la sede legale da un'anagrafica.
