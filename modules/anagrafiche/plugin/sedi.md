---
title: Plugin Sedi
description: Guida al plugin Sedi in OpenSTAManager
---

# Sedi

{% hint style="info" %}
Il plugin **Sedi** è una componente del modulo **Anagrafiche** dedicata alla completa gestione di tutte le eventuali sedi delle anagrafiche registrate all'interno di OpenSTAManager.
{% endhint %}

## Navigazione

Il plugin è raggiungibile, all'interno dell'area di modifica di un _record_ del modulo **Anagrafiche**, attraverso il menu dedicato sotto la dicitura **Sedi**.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FjoZwwA0nmHwTOgrrIB69%2Ffile.png?alt=media)

## Caratteristiche

La schermata principale del plugin è strutturata secondo la tabella generale predefinita, presentando inoltre la possibilità di creare e modificare gli elementi attraverso strutture grafiche che si sovrappongono agli altri contenuti (_modal_).

### Creazione

La creazione di nuovi elementi segue il funzionamento standard del gestionale, necessitando il click sul pulsante apposito all'interno dell'intestazione del plugin.

Viene quindi reso possibile compilare tutte le informazioni di base relative alla nuova sede da creare:

* Nome sede
* Indirizzo
* Codice destinatario
* Città
* CAP
* Provincia
* Km
* Nazione
* Zona (per maggiori informazioni, visitare la documentazione del modulo [**Zone**](../zone.md))
* Cellulare
* Telefono
* Indirizzo email

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2F0moxETvNmaEd7gYJsBLx%2Ffile.png?alt=media)

### Modifica

La schermata di modifica, sebbene molto simile a quella di creazione, permette in particolare di impostare altre informazioni secondarie.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FFkZ2iucjuXlwBDU44Fhf%2Ffile.png?alt=media)

In particolare, se l'impostazione [**Google Maps API key**](broken-reference) viene impostata, sarà possibile visualizzare attraverso Google Maps l'indirizzo indicato ed eventualmente definire manualmente longitudine e latitudine.

## Particolarità

{% hint style="info" %}
La sede legale, predefinita per l'anagrafica, non viene registrata allo stesso modo delle altre sedi. Sarà pertanto impossibile eliminare completamente la sede legale da un'anagrafica.
{% endhint %}
