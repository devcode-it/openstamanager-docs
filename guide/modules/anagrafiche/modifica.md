---
title: Modifica anagrafica
---

# Modifica

La sezione di modifica degli elementi del modulo segue il sistema standard del gestionale, necessitando il click sulla riga relativa al _record_ all'interno della tabella della schermata principale.

## Caratteristiche

Una volta all'interno di questa parte del sistema, il modulo **Anagrafiche** permette di completare _tutte_ le informazioni che il gestionale supporta per le anagrafiche. In particolare, per permettere un maggiore senso logico nella navigazione dei dati, la sezione di modifica è suddivisa in 6 raggruppamenti:

* [Dati anagrafici](modifica.md#dati-anagrafici)
* [Sede legale](modifica.md#sede-legale)
* [Acquisti](modifica.md#acquisti)
* [Vendite](modifica.md#vendite)
* [Informazione aggiuntive](modifica.md#informazioni-aggiuntive)
* [Allegati](modifica.md#allegati)

### Dati anagrafici

Il primo raggruppamento di informazioni sull'anagrafica consiste nell'insieme dei dati anagrafici relativi.

Attraverso questa sezione, è possibile procedere alla modifica delle informazioni di base dell'anagrafica in questione:

* Ragione sociale
* Tipologia \(Azienda/Privato/Ente pubblico\)
* Informazioni sulla nascita \(o fondazione\)
* Sesso
* Codice interno dell'anagrafica
* Indirizzo PEC
* Sito web

![Screenshot modifica anagrafica](../../../.gitbook/assets/datianagrafici.PNG)

### Sede legale

Viene quindi presentata una selezione di campi relativi alle informazioni sulla _sede legale_ dell'anagrafica, quali:

* Partita IVA
* Codice fiscale
* Informazioni varie sulla sede \(per maggiori informazioni, visitare la sezione [Sedi](plugin/sedi.md)\)

In particolare, se l'impostazione [**Google Maps API key**](maps.md) viene impostata, sarà possibile visualizzare attraverso Google Maps l'indirizzo indicato ed eventualmente definire manualmente longitudine e latitudine.

![Screenshot sezione sede legale](../../../.gitbook/assets/sedelegale.PNG)

### Acquisti

Raggruppamento che viene visualizzato solamente se si modifica un **Fornitore,** permette di impostare dei valori predefiniti di:

* Pagamento 
* Iva
* Listino articoli
* Banca 
* Ritenuta d'acconto
* Piano dei conti fornitore

![Screenshot sezione acquisti](../../../.gitbook/assets/acquisti.PNG)

### Vendite

Raggruppamento che viene visualizzato solamente se si modifica un **Cliente,** permette di impostare dei valori predefiniti di:

* Pagamento
* Iva
* Listino articoli
* Tipo attività predefinito 
* Piano dei conti cliente\(valore fisso\)

![Screenshot sezione vendite](../../../.gitbook/assets/vendite.PNG)

### Informazioni aggiuntive

L'ultimo raggruppamento di informazioni presenta una serie di elementi non fondamentali per ogni tipologia di anagrafica, ma che potrebbero essere utili in base alle necessità dell'utente \(tra cui la possibilità di cambiare la tipologia dell'anagrafica\).

![Screenshot sezione informazioni aggiuntive](../../../.gitbook/assets/informazioniaggiuntive.PNG)

### Allegati

In questa sezione è possibile caricare un file dal proprio computer specificandone la categoria.

{% hint style="warning" %}
**Attenzione:** Selezionando l'anagrafica **Azienda** è possibile impostare il logo dell'azienda, caricando un file immagine \(jpg,png,...\) con risoluzione 302 x 111 , specificando sul campo **Nuovo allegato** il nome **Logo stampe**. Il logo caricato su questa anagrafica permetterà di visualizzare in tutte le stampe cartacee il logo precedentemente caricato\( ad esempio sulla stampa di una attività, di una fattura di vendita, di un  preventivo, etc...\)
{% endhint %}

![Screenshot sezione allegati](../../../.gitbook/assets/allegati%20%281%29.PNG)

## Altro

In alcuni casi, l'eliminazione dell'anagrafica viene impedita.

Questa condizione si verifica quando esiste un collegamento interno dell'elemento con altre componenti del gestionale.

![Screenshot documenti collegati](../../../.gitbook/assets/doccollegati.PNG)

Una volta completata la creazione del nuovo elemento anagrafico, il gestionale provvederà a creare i relativi conti per il **Partitario** se l'anagrafica è di tipo _Cliente_ oppure _Fornitore_.

## Fatturazione Elettronica

{% hint style="info" %}
Per quanto riguarda la **Fatturazione Elettronica** è stata creata una sezione apposita, [clicca qui](../../../faq-1/fatturazione-elettronica/) per visualizzarla!
{% endhint %}

