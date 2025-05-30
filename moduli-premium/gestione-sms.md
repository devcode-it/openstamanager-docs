---
description: Guida al modulo aggiuntivo Gestione SMS in OpenSTAManager
---

# 📗 Gestione SMS

{% hint style="info" %}
**Gestione SMS** è un modulo acquistabile da **OpenstaSTAManager** che permette l'invio di SMS dall'interno dei moduli, definiti da specifici template e tenendo traccia dello storico degli sms inviat&#x69;**.**
{% endhint %}

Nel menù verranno aggiunte le seguenti voci:

<figure><img src="../.gitbook/assets/immagine (327).png" alt=""><figcaption></figcaption></figure>

* Template SMS
* Coda SMS
* Gestione SMS
  * Account SMS

#### Template SMS

In questo modulo è possibile creare nuovi template per l'invio di SMS

<figure><img src="../.gitbook/assets/immagine (325).png" alt=""><figcaption></figcaption></figure>

La creazione dei template può includere diverse variabili definite dal modulo che si seleziona al momento della creazione del template.

<figure><img src="../.gitbook/assets/immagine (820).png" alt=""><figcaption></figcaption></figure>

#### Coda SMS

In questo modulo è possibile tenere traccia degli sms inviati, degli sms in uscita, e di quelli non inviati.

<figure><img src="../.gitbook/assets/immagine (634).png" alt=""><figcaption></figcaption></figure>

#### Account SMS

In questo modulo è possibile configurare un account con un provider di invio SMS, attualmente è supportata la configurazione unicamente con [Smshosting](https://www.smshosting.it/it?utm_campaign=Brand-Protection\&utm_source=GoogleAds\&term=smshosting\&matchtype=b\&utm_medium=g\&dvc=c\&adpos=\&gad=1\&gclid=Cj0KCQjwr82iBhCuARIsAO0EAZyr9CrNsl9qAvwARwzNLOo0eEJqO2IiNRswHP7-8Uk6BzOCBcmUIzAaAgn3EALw_wcB).

<figure><img src="../.gitbook/assets/immagine (826).png" alt=""><figcaption></figcaption></figure>

Si dovranno quindi configurare:

* **Nome account:** a scelta
* **Provider:** smshosting
* **Auth key** e **Auth secret**: è possibile trovare i seguenti dati all'interno del proprio account smshosting

Accedendo al modulo **Sviluppatori**

<figure><img src="../.gitbook/assets/immagine (483).png" alt=""><figcaption></figcaption></figure>

Cliccando su API REST, HTTP e SOAP

<figure><img src="../.gitbook/assets/immagine (630).png" alt=""><figcaption></figcaption></figure>

I dati da inserire nella configurazione sono evidenziati nel riquadro azzurro.

<figure><img src="../.gitbook/assets/immagine (828).png" alt=""><figcaption></figcaption></figure>

Andando ora all'interno di un modulo di cui è stato creato un template SMS sarà possibile procedere all'invio selezionando il template interessato:

<figure><img src="../.gitbook/assets/immagine (835).png" alt=""><figcaption></figcaption></figure>

Il numero di telefono a cui inviare l'SMS verrà autocompilato con il numero presente nell'anagrafica cliente selezionata.

<figure><img src="../.gitbook/assets/immagine (310).png" alt=""><figcaption></figcaption></figure>
