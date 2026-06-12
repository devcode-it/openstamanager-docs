---
description: Come aggiornare OpenSTAManager
---

# 🆙 Aggiornamento

## Guida all'installazione da versioni precedenti:

### Aggiornamento da versione <= 2.4.54

{% hint style="info" %}
Con il passaggio da OSM 2.4.54 a OSM 2.5 sono cambiati i requisiti di php del gestionale, è ora richiesta una versione minima di php8.1, massima di php8.3.

Per poter utilizzare le versioni a partire dalla 2.5 è pertanto necessario effettuare l'aggiornamento estraendo manualmente lo zip della release all'interno della directory in cui si trova il gestionale.
{% endhint %}

### Aggiornamento da versione <= 2.7.x

{% hint style="info" %}
Con l'aggiornamento di alcune librerie di composer nella versione 2.8, per poter aggiornare il gestionale potrebbe essere necessario cancellare la cartella vendor ed estrarre manualmente i file presenti nella release nella root del gestionale. Questo perchè vecchi file presenti in vendor danno errore in fase di aggiornamento. A partire dalla versione 2.8.1 la sovrascrittura completa della cartella vendor è stata gestita.
{% endhint %}

### Aggiornamento da versione <= 2.9.x

{% hint style="info" %}
A causa di una nuova funzione introdotta nella versione 2.10 (GetWidgets), l'aggiornamento darà errore e sarà necessario aggiornare la pagina per procedere all'aggiornamento del database. A questo punto partirà l'aggiornamento database ma darà errore per lo stesso motivo, si rende necessario **procedere all'aggiornamento aggiungendo all'url ?force=1.**

Questo non comporta alcun tipo di problema nell'utilizzo del gestionale, è unicamente un'aggiunta di funzione non gestita, gestita a partire dalla versione 2.10.
{% endhint %}

### Aggiornamento da versione <= 2.10.x

{% hint style="info" %}
A partire dalla versione 2.11, le versioni di php < php8.3 non sono più supportate, consigliamo pertanto di verificare di poter impostare questa versione di php sul server PRIMA di effettuare l'aggiornamento.

La compatibilità con MySQL è stata invece estesa alla versione 8.4, ed è stata introdotta la compatibilità con MariaDB >= 10.5
{% endhint %}

{% hint style="info" %}
Inoltre, in questa versione sono stati introdotti importanti cambi strutturali del database, consigliamo di verificare dal modulo Aggiornamenti che non ci siano incongruenze a livello di database, altrimenti non trovando corrispondenza le query in fase di aggiornamento daranno errore.

A seguito di questo aggiornamento si renderà quindi necessario aggiornare tutte le eventuali viste custom presenti, e ogni personalizzazione o modifica rispetto alla versione Community edition del gestionale, oltre che aggiornare eventuali moduli premium del gestionale, pertanto consigliamo di verificare **prima** dell'aggiornamento, con lo staff di assistenza, la loro disponibilità.
{% endhint %}

## Come aggiornare

La procedura corretta per installare i nuovi aggiornamenti di OSM è:

* eseguire i controlli di integrità del database e correggere ogni errore segnalato, in modo da evitare che le query diano errore in fase di aggiornamento: [https://docs.openstamanager.com/v/2.11/guide/esempi/verificare-linstallazione-di-osm#controllo-sul-database](https://docs.openstamanager.com/v/2.11/guide/esempi/verificare-linstallazione-di-osm#controllo-sul-databaseverificare)
* **effettuare un backup del gestionale**
* cambiare versione di php se necessario, con una versione compatibile
* estrarre lo zip della release all'interno della root del gestionale
* seguire la procedura guidata dell'aggiornamento, cliccando sul tasto Aggiorna!

{% hint style="info" %}
Nel caso di aggiornamento da vecchie versioni consigliamo di cancellare il file config.inc.php e di ricrearlo tramite procedura guidata, che si avvierà automaticamente al primo accesso al gestionale.
{% endhint %}

### Errori di aggiornamento

La procedura di aggiornamento, come ogni componente software, è soggetta a possibili errori.

<figure><img src="../../.gitbook/assets/immagine (359).png" alt=""><figcaption></figcaption></figure>

In questi casi, si consiglia di contattare gli sviluppatori ufficiali e di consultare il [forum ufficiale](https://www.openstamanager.com/forum/) per eventuali segnalazioni simili.

### Aggiornamento in corso

{% hint style="info" %}
Mentre l'aggiornamento è in esecuzione, il gestionale rimarrà bloccato per tutti gli utenti ad eccezione di quello responsabile dell'inizio della procedura di aggiornamento.

Nel caso la procedura rimanga persistente per un periodo molto prolungato di tempo, è possibile che si sia verificato un errore non rilevato dall'utente durante l'aggiornamento. In questo caso si consiglia di consultare la sezione di [Ripresa forzata](aggiornamento.md#ripresa-forzata) oppure di contattare gli sviluppatori ufficiali.
{% endhint %}

### Ripresa forzata

In alcuni casi particolari, può essere necessario riprendere forzatamente l'esecuzione di un aggiornamento andato in errore.

Questo viene reso possibile visitando l'URL a cui è possibile accedere a OpenSTAManager con l'aggiunta del testo `?force=1`.&#x20;

{% hint style="warning" %}
**Attenzione**: quest'azione è sconsigliata a utenti non esperti.
{% endhint %}
