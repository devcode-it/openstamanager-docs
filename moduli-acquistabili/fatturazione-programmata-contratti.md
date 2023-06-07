---
description: >-
  Guida al modulo aggiuntivo Fatturazione programmata contratti in
  OpenSTAManager
---

# 📗 Fatturazione programmata contratti

{% hint style="info" %}
Il modulo **Fatturazione programmata contratti** permette di pianificare la rateizzazione di un contratto impostando l'emissione automatica di una fattura di vendita e invio via email della copia di cortesia al cliente.
{% endhint %}

Dopo aver installato il modulo è possibile andare a definire la pianificazione della fatturazione dei contratti esistenti, oppure [creare un nuovo contratto](../openstamanager/modules/vendite/contratti/#creazione).

Per pianificare la fatturazione è sufficiente accedere al plugin Ricorrenza fatturazione, dal contratto scelto.

<figure><img src="../.gitbook/assets/immagine (271).png" alt=""><figcaption></figcaption></figure>

Da qui sarà possibile definire la ricorrenza di fatturazione, la data di inizio e l'importo che dovrà avere ogni rata.

<figure><img src="../.gitbook/assets/immagine (286).png" alt=""><figcaption></figcaption></figure>

Ora, se lo stato del contratto è "In lavorazione", sarà possibile visualizzare le rate da fatturare dal modulo **Fatturazione contratti**.

<figure><img src="../.gitbook/assets/immagine (273).png" alt=""><figcaption></figcaption></figure>

Volendo fatturare le rate manualmente, sarà sufficiente selezionare le rate interessate e cliccare su Crea fattura. Da qui sarà possibile selezionare se accodare le rate selezionate a fatture della stessa anagrafica in stato Bozza, e modificare la data, il sezionale e il tipo di fattura.

<figure><img src="../.gitbook/assets/immagine (285).png" alt=""><figcaption></figcaption></figure>

Cliccando su Crea fatture si procede alla fatturazione delle rate selezionate:

<figure><img src="../.gitbook/assets/immagine (281).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
E' possibile procedere alla fatturazione automatica delle rate tramite uno script impostato in cron, che provvederà alla fatturazione come da configurazione, con possibilità di inviare copia di cortesia via mail ai clienti.
{% endhint %}

