---
description: Come aggiornare OpenSTAManager
---

# 🆙 Aggiornamento

{% hint style="info" %}
Con il passaggio da OSM 2.4.54 a OSM 2.5.3 sono cambiati i requisiti di php del gestionale. Per poter utilizzare le versioni a partire dalla 2.5.3 è pertanto necessario effettuare l'aggiornamento via file.
{% endhint %}

La procedura corretta per installare i nuovi aggiornamenti di OSM è:

* eseguire i controlli di integrità del database e correggere ogni errore segnalato, in modo da evitare che le query diano errore in fase di aggiornamento: [https://docs.openstamanager.com/v/2.5.4/guide/esempi/verificare-linstallazione-di-osm#controllo-sul-database](https://docs.openstamanager.com/v/2.5.4/guide/esempi/verificare-linstallazione-di-osm#controllo-sul-database)
* **effettuare un backup del gestionale**
* cambiare versione di php in php>=8.1
* estrarre lo zip della release all'interno della root del gestionale
* seguire la procedura guidata dell'aggiornamento, cliccando sul tasto Aggiorna!

<figure><img src="../../.gitbook/assets/immagine (198).png" alt=""><figcaption></figcaption></figure>

Al termine dell'aggiornamento si presenterà la seguente schermata.​

<figure><img src="../../.gitbook/assets/immagine (199).png" alt=""><figcaption></figcaption></figure>

## ⚠️ Errori di aggiornamento

La procedura di aggiornamento, come ogni componente software, è soggetta a possibili errori.

<figure><img src="../../.gitbook/assets/immagine (200).png" alt=""><figcaption></figcaption></figure>

In questi casi, si consiglia di contattare gli sviluppatori ufficiali e di consultare il [forum ufficiale](https://www.openstamanager.com/forum/) per eventuali segnalazioni simili.

## 🔄 Aggiornamento in corso

{% hint style="info" %}
Mentre l'aggiornamento è in esecuzione, il gestionale rimarrà bloccato per tutti gli utenti ad eccezione di quello responsabile dell'inizio della procedura di aggiornamento.

Nel caso la procedura rimanga persistente per un periodo molto prolungato di tempo, è possibile che si sia verificato un errore non rilevato dall'utente durante l'aggiornamento. In questo caso si consiglia di consultare la sezione di [Ripresa forzata](aggiornamento.md#ripresa-forzata) oppure di contattare gli sviluppatori ufficiali.
{% endhint %}

### 🔃 Ripresa forzata

In alcuni casi particolari, può essere necessario riprendere forzatamente l'esecuzione di un aggiornamento andato in errore.

Questo viene reso possibile visitando l'URL a cui è possibile accedere a OpenSTAManager con l'aggiunta del testo `?force=1`.&#x20;

{% hint style="warning" %}
**Attenzione**: quest'azione è sconsigliata a utenti non esperti.
{% endhint %}
