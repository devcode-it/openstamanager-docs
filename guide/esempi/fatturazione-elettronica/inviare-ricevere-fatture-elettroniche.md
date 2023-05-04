---
description: Come inviare fatture elettroniche allo SDI e come scaricarne le ricevute.
---

# 📩 Ricevute FE

Acquistando uno dei pacchetti OpenSTAManager con incluso l'invio e la ricezione delle fatture elettroniche si potrà gestire la propria fatturazione dal gestionale, dopo aver configurato la propria API key in Strumenti/Impostazioni/Fatturazione elettronica/OSMCloud Services API Token.

### ✉️ Invio delle fatture elettroniche

Nella versione corrente del gestionale sarà sufficiente impostare lo stato di una fattura su _Emessa_ per generare l'XML della fattura elettronica da inviare.

Accedendo al plugin Fatturazione Elettronica, sarà possibile: rigenerare il documento, visualizzarlo, scaricarlo, inviarlo o verificare le eventuali notifiche dallo SDI presenti.

Si dovrà quindi ora procedere a cliccare su Invia per mandare la fattura appena emessa allo SDI, che prenderà quindi lo stato _Inviata_.

<figure><img src="../../../.gitbook/assets/immagine (245).png" alt=""><figcaption></figcaption></figure>

### ✉️ Importazione delle ricevute dallo SDI

Dopo qualche giorno dall'invio delle fatture elettroniche, si dovrà provvedere a scaricare le ricevute dallo SDI.

Si dovrà quindi dal modulo Vendite/Fatture di vendita cliccare sul plugin **Ricevute FE/Ricerca ricevute** e in seguito procedere a importarle facendo clic sul tasto Importa tutte le ricevute.

<figure><img src="../../../.gitbook/assets/immagine (470).png" alt=""><figcaption></figcaption></figure>

Il campo stato ora potrà riportare uno dei seguenti valori:

* **AT - Attestazione trasmissione,** messaggio che il SDI invia al trasmittente nei casi di impossibilità di recapito del file all’amministrazione destinataria per cause non imputabili al trasmittente (amministrazione non individuabile all’interno dell’_Indice delle Pubbliche Amministrazioni_ oppure problemi di natura tecnica sul canale di trasmissione);
* **DT - Decorrenza termini**, a valere solo sulle fatture inviate a Pubblica Amministrazione, il Sistema di Interscambio invia la ricevuta di decorrenza termini dopo l’inoltro di una fattura elettronica all’ufficio PA destinatario, quando quest’ultimo non risponde con “Notifica di esito” (positivo o negativo) entro 15 giorni. La fattura si considera quindi implicitamente accettata dal destinatario PA.
* **EC01 - Accettata**, la fattura elettronica è stata recapitata correttamente al sistema ricevente del cliente, oltre che al suo cassetto fiscale.
* **EC02 - Rifiutata**, la fattura elettronica è stata rifiutata dalla PA, che solitamente provvede a notificarne il motivo.
* **ERR - Trasmissione non riuscita**, errore interno del gestionale
* **ERVAL - Errore di validazione**, errore di validazione del file XML prima di essere inviato allo SDI&#x20;
* **MC - Mancata consegna**, la fattura elettronica è stata correttamente recapitata solo al cassetto fiscale del cliente poiché il cliente non possiede un sistema ricevente oppure non ha fornito un codice univoco o una PEC.
* **NE - Notifica esito,** messaggio con il quale il SdI inoltra al trasmittente la _notifica di esito committente_ eventualmente ricevuta dal destinatario della fattura;
* **NS - Scartata**, la fattura elettronica non ha passato il controllo della Agenzia delle Entrate, la quale indica il motivo dello scarto.
* **QUEUE - In coda di elaborazione**, indica che la fattura è stata messa in coda tramite l'azione di gruppo per essere inviata allo SDI
* **RC - Consegnata**, la fattura elettronica è stata correttamente consegnata e accettata dalla PA.
* **Inviata**, nel caso la fattura non sia ancora stata elaborata dallo SDI.

{% hint style="danger" %}
Nel caso in cui ci sia necessità di modificare una fattura elettronica già depositata allo SDI, si dovrà procedere ad emettere una nota di credito per annullare la fattura in questione e a inviare una nuova fattura riportando i dati corretti.
{% endhint %}



