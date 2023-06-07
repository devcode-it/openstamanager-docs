---
description: Come modificare un'anagrafica con OpenSTAManager
---

# 🖌 Modifica

Per modificare un'anagrafica si dovrà cliccare sul record interessato per aprire la schermata di dettaglio. Da qui sarà possibile completare e modificare _tutte_ le informazioni che il gestionale supporta per le anagrafiche.

In questa schermata sarà possibile distinguere 6 diverse sezioni:

* Dati anagrafici
* Sede legale
* Geolocalizzazione
* Informazioni per tipo di anagrafica
* Informazione aggiuntive
* Allegati
* Documenti collegati

## 👦 Dati anagrafici

Nella prima sezione è possibile procedere alla modifica delle informazioni di base dell'anagrafica in questione:

* Denominazione (Ragione sociale o Nome e Cognome)
* Partita IVA
* Tipologia (Azienda/Privato/Ente pubblico)
* Codice Fiscale
* Codice anagrafica
* Codice destinatario
* PEC
* Sito web

<figure><img src="../../../.gitbook/assets/immagine (117).png" alt=""><figcaption></figcaption></figure>

## 🏭 Sede legale

Nella seconda sezione è possibile trovare:

* Indirizzo
* C.A.P.
* Città
* Provincia
* Nazione
* Telefono
* Cellulare
* Email
* Fax
* Zona
* Distanza
* Opt-out per newsletter (attivando questa opzione l'anagrafica verrà esclusa dai destinatari di eventuali Newsletter)

![](<../../../.gitbook/assets/immagine (379).png>)

## 🗺️ Geolocalizzazione

{% hint style="info" %}
In questa sezione è possibile visualizzare attraverso _Google Maps_ l'indirizzo indicato ed eventualmente definire manualmente latitudine e longitudine.
{% endhint %}

Per fare ciò basta cliccare sopra il link mostrato all'interno del riquadro:

<figure><img src="../../../.gitbook/assets/immagine (269).png" alt=""><figcaption></figcaption></figure>

Successivamente si verrà indirizzati in _impostazioni_ per inserire un [_Google Maps API Key_ ](../../../configurazioni/configurazione-google-maps-api-key.md)valido.

Andando a inserire questa chiave in Strumenti/Impostazioni/API/Google Maps API key, dall'anagrafica cliente sarà ora possibile visualizzare la sua locazione in Geolocalizzazione.

![](<../../../.gitbook/assets/image (560).png>)

## ℹ️ Informazioni per tipo di anagrafica

In questa sezione si possono impostare dei valori predefiniti in base al tipo di anagrafica:

### 👨 Cliente

* Provenienza cliente
* Pagamento predefinito
* Banca predefinita per accrediti
* IVA predefinita
* Ritenuta d'acconto predefinita
* Piano di sconto/magg. su articoli
* Indirizzo di fatturazione
* Agente principale
* Agenti secondari
* Listino
* Tipo attività predefinita
* Dichiarazione d'intento
* Piano dei conti cliente

<figure><img src="../../../.gitbook/assets/immagine (138).png" alt=""><figcaption></figcaption></figure>

### 💁‍♂️ Fornitore

* Pagamento predefinito
* Iva predefinita
* Piano di sconto/magg. su articoli
* Banca predefinita per addebiti
* Ritenuta d'acconto predefinita
* Piano dei conti fornitore

![](<../../../.gitbook/assets/immagine (96).png>)

### 🧑‍💼 Cliente e Fornitore

* Abilitare lo split payment
* Relazione
* Dicitura fissa in fattura

<figure><img src="../../../.gitbook/assets/immagine (104).png" alt=""><figcaption></figcaption></figure>

### 🧑‍🔧 Tecnico

* Colore

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FgBkRUQGtr08yMCBhTgsA%2Ffile.png?alt=media)

## ⌨️ Informazioni aggiuntive

In questa sezione include elementi non fondamentali per ogni tipologia di anagrafica, ma che potrebbero essere utili in base alle necessità dell'utente.

E' qui possibile trovare le informazioni relative a:

* Numero d'iscrizione registro imprese
* Codice R.E.A.
* Riferimento Amministrazione
* Provvigione predefinita (nel caso di anagrafica del tipo Agente)
* Numero di iscrizione al tribunale
* Numero di iscrizione all'albo degli artigiani
* Foro di competenza
* Capitale sociale
* Settore merceologico
* Marche trattate
* Numero dipendenti
* Numero macchine
* Tipo di anagrafica
* Note

![](<../../../.gitbook/assets/immagine (79).png>)

{% hint style="info" %}
Impostando una provvigione predefinita per un agente, essa verrà proposta in percentuale nelle righe dei documenti creati legati all'agente selezionato.&#x20;

Sarà possibile visualizzare poi il totale della provvigione tra i valori del documento.
{% endhint %}

## 🛄 Allegati

In questa sezione è possibile caricare un file dal proprio computer specificandone la categoria.

{% hint style="warning" %}
**Attenzione:** Selezionando l'anagrafica **Azienda** è possibile impostare il logo dell'azienda, caricando un file immagine con risoluzione 302 x 111 , e modificandone il campo **Nome** con **"Logo stampe"**.

Questo permetterà di visualizzare in tutte le stampe cartacee il logo appena caricato.
{% endhint %}

![](<../../../.gitbook/assets/immagine (289).png>)

{% content-ref url="../../../guide/esempi/impostare-logo-nelle-stampe.md" %}
[impostare-logo-nelle-stampe.md](../../../guide/esempi/impostare-logo-nelle-stampe.md)
{% endcontent-ref %}

## 🗳️ Altro

Quando esiste un collegamento interno di un'anagrafica con altre componenti del gestionale, la sua eliminazione non è consentita.

![Screenshot documenti collegati](../../../.gitbook/assets/DocCollegati.PNG)
