---
description: >-
  Guida all'impostazione dell'invio automatico dei solleciti di pagamento con
  OpenSTAManager
---

# 🫴 Invio automatico di solleciti di pagamento

Da Strumenti/Impostazioni/Scadenzario è possibile configurare l'invio dei solleciti in automatico:&#x20;

<figure><img src="../../.gitbook/assets/immagine.png" alt=""><figcaption></figcaption></figure>

Attivando l'impostazione **Invio solleciti in automatico,** essa verrà eseguita una volta al giorno, in base all'impostazione del task.

Potete verificare le impostazioni del task da Strumenti/Gestione task, in questo caso viene eseguito tutti  giorni alle ore 7.00 del mattino:

<figure><img src="../../.gitbook/assets/immagine (1093).png" alt=""><figcaption></figcaption></figure>

Dalle impostazioni dell'invio dei solleciti è possibile trovare le seguenti configurazioni:

* **Template email primo sollecito**: template email utilizzato per il primo sollecito di pagamento di una rata scaduta.
* **Ritardo in giorni della scadenza della fattura per invio sollecito pagamento**: numero di giorni dopo i quali verrà inviato il primo sollecito di pagamento, utilizzando il template selezionato nell'impostazione precedente.
* **Ritardo in giorni dell'ultima email per invio sollecito pagamento**: numero di giorni a partire dalla data di invio del sollecito precedente, allo scadere dei quali verranno inviati il secondo e terzo sollecito e la notifica di mancato pagamento.
* **Template email secondo sollecito**: template email utilizzato per il secondo sollecito di pagamento di una rata scaduta.
* **Template email terzo sollecito**: template email utilizzato per il terzo sollecito di pagamento di una rata scaduta.
* **Template email mancato pagamento dopo i solleciti**: template email utilizzato per la notifica di mancato pagamento a seguito dell'invio di 3 solleciti, all'indirizzo selezionato nell'impostazione successiva.
* **Indirizzo email mancato pagamento dopo i solleciti**: indirizzo email sul quale verrà notificato il mancato pagamento a seguito dell'invio di 3 solleciti al cliente, allo scadere dei giorni previsti per la notifica scadenza se l'incasso del pagamento non viene registrato.
* **Template email promemoria scadenza**: template email utilizzato per la notifica dell'imminente scadenza con giorni di anticipo definiti nell'impostazione successiva.
* **Intervallo di giorni in anticipo per invio promemoria scadenza:** specifica il numero di giorni alla scadenza in cui inviare un promemoria di pagamento notificando la scadenza imminente
