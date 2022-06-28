---
title: Modifica anagrafica
description: Come modificare un'anagrafica con OpenSTAManager
---

# 🖌 Modifica

Per modificare un'anagrafica si dovrà cliccare sul record interessato per aprire la schermata di dettaglio. Da qui sarà possibile completare e modificare _tutte_ le informazioni che il gestionale supporta per le anagrafiche.&#x20;

In questa schermata sarà possibile distinguere 6 diverse sezioni:

* [Dati anagrafici](modifica.md#dati-anagrafici)
* [Sede legale](modifica.md#sede-legale)
* [Geolocalizzazione](modifica.md#geolocalizzazione)
* [Informazioni per tipo di anagrafica](modifica.md#informazioni-per-tipo-di-anagrafica)
* [Informazione aggiuntive](modifica.md#informazioni-aggiuntive)
* [Allegati](modifica.md#allegati)

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

![](<../../.gitbook/assets/immagine (20).png>)

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

![](<../../.gitbook/assets/immagine (36).png>)

## 🗺️ Geolocalizzazione

{% hint style="info" %}
In questa sezione è possibile visualizzare attraverso _Google Maps_ l'indirizzo indicato ed eventualmente definire manualmente latitudine e longitudine.
{% endhint %}

Per fare ciò basta cliccare sopra il link mostrato all'interno del riquadro:

![](<../../.gitbook/assets/immagine (50).png>)

Successivamente si verrà indirizzati in _impostazioni_ per inserire un _Google Maps API Key_ valido.

### 🌎 Come ottenere un Google Maps API Key

Cliccare su questo link: [https://cloud.google.com/maps-platform/?\_\_utma=102347093.1283278314.1550498378.1550499031.1550499031.1&\_\_utmb=102347093.0.10.1550499031&\_\_utmc=102347093&\_\_utmx=-&\_\_utmz=102347093.1550499031.1.1.utmcsr=google|utmccn=(organic)|utmcmd=organic|utmctr=(not provided)&\_\_utmv=-&\_\_utmk=128107788&\_ga=2.39899682.1839265660.1550498378-1283278314.1550498378#get-started](https://cloud.google.com/maps-platform/?\_\_utma=102347093.1283278314.1550498378.1550499031.1550499031.1&\_\_utmb=102347093.0.10.1550499031&\_\_utmc=102347093&\_\_utmx=-&\_\_utmz=102347093.1550499031.1.1.utmcsr=google%7Cutmccn=%28organic%29%7Cutmcmd=organic%7Cutmctr=%28not%20provided%29&\_\_utmv=-&\_\_utmk=128107788&\_ga=2.39899682.1839265660.1550498378-1283278314.1550498378#get-started)

Apparirà questa schermata:

![](<../../.gitbook/assets/immagine (7).png>)

Spuntare tutte e 3 le caselle (Maps API, Geocoding API, Places API) e premere ![](<../../.gitbook/assets/immagine (69).png>)

Accedere ora con email e password in caso non si fosse già effettuato l'accesso a google.

Apparirà ora questa schermata in cui si deve selezionare Yes, e premere il tasto NEXT.

![](<../../.gitbook/assets/immagine (52).png>)

Apparirà ora la schermata in cui si dovrà andare a creare un account di fatturazione seguendo il tasto in basso.

![](<../../.gitbook/assets/immagine (42).png>)

Da qui, si dovranno accettare i termini di servizio, compilare i campi richiesti e cliccare su Avvia la mia prova gratuita.

{% hint style="warning" %}
**Attenzione:** Mettendo i dati della carta di credito non verrà fatto alcun addebito, sono richiesti solamente per verifica. Se si prova in qualche modo a saltare l'inserimento del metodo di pagamento e a generare comunque l'API, essa non funzionerà. L'inserimento del metodo di pagamento è obbligatorio.
{% endhint %}

Successivamente cliccare sulle 3 linee in alto a sinistra, andare su API e servizi e selezionare Credenziali.

![](<../../.gitbook/assets/immagine (41).png>)

Dalla schermata che si presenta ora, si dovrà cliccare su Crea credenziali e selezionare Chiave API. Ora la chiave API è stata creata.

![](<../../.gitbook/assets/immagine (8).png>)

Andando a inserire questa chiave in Strumenti/Impostazioni/API/Google Maps API key, dall'anagrafica cliente sarà ora possibile visualizzare la sua locazione in Geolocalizzazione.

![](<../../.gitbook/assets/immagine (38).png>)

## ℹ️ Informazioni per tipo di anagrafica

In questa sezione si possono impostare dei valori predefiniti in base al tipo di anagrafica:

### 👨 Cliente

* Provenienza cliente
* Pagamento predefinito
* IVA predefinita
* Piano di sconto/magg. su articoli
* Agente principale
* Piano dei conti cliente\*
* Relazione con il cliente
* Banca predefinita per accrediti
* Ritenuta d'acconto predefinita
* Indirizzo di fatturazione
* Agenti secondari
* Tipo attività predefinita

![](<../../.gitbook/assets/immagine (17).png>)

### 💁‍♂️ Fornitore

* Pagamento predefinito
* Iva predefinita
* Piano di sconto/magg. su articoli
* Banca predefinita per addebiti
* Ritenuta d'acconto predefinita
* Piano dei conti fornitore\*

![](<../../.gitbook/assets/immagine (64).png>)

### 🧑‍💼 Cliente e Fornitore

* Abilitare lo split payment
* Dicitura fissa in fattura

![](<../../.gitbook/assets/immagine (49).png>)

### 🧑‍🔧 Tecnico

* Colore

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FgBkRUQGtr08yMCBhTgsA%2Ffile.png?alt=media)

## ⌨️ Informazioni aggiuntive

In questa sezione include elementi non fondamentali per ogni tipologia di anagrafica, ma che potrebbero essere utili in base alle necessità dell'utente.

![](<../../.gitbook/assets/immagine (37).png>)

## 🛄 Allegati

In questa sezione è possibile caricare un file dal proprio computer specificandone la categoria.

{% hint style="warning" %}
**Attenzione:** Selezionando l'anagrafica **Azienda** è possibile impostare il logo dell'azienda, caricando un file immagine con risoluzione 302 x 111 , e modificandone il campo **Nome** con **"Logo stampe"**.

Questo permetterà di visualizzare in tutte le stampe cartacee il logo appena caricato.
{% endhint %}

![](<../../.gitbook/assets/immagine (68).png>)

## 🗳️ Altro

Quando esiste un collegamento interno di un'anagrafica con altre componenti del gestionale, la sua eliminazione non è consentita.

![Screenshot documenti collegati](../../.gitbook/assets/DocCollegati.PNG)

\*Se l'anagrafica che si va a creare è del tipo cliente o fornitore, una volta completata la sua creazione, il gestionale provvederà a creare i relativi conti nel piano dei conti.
