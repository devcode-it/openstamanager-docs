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

<figure><img src="../.gitbook/assets/immagine (74).png" alt=""><figcaption></figcaption></figure>

Da qui sarà possibile definire la ricorrenza di fatturazione, la data di inizio e l'importo che dovrà avere ogni rata.

<figure><img src="../.gitbook/assets/immagine (531).png" alt=""><figcaption></figcaption></figure>

Ora, se lo stato del contratto è "In lavorazione", sarà possibile visualizzare le rate da fatturare dal modulo **Fatturazione contratti**.

<figure><img src="../.gitbook/assets/immagine (349).png" alt=""><figcaption></figcaption></figure>

Volendo fatturare le rate manualmente, sarà sufficiente selezionare le rate interessate e cliccare su Crea fattura. Da qui sarà possibile selezionare se accodare le rate selezionate a fatture della stessa anagrafica in stato Bozza, e modificare la data, il sezionale e il tipo di fattura.

<figure><img src="../.gitbook/assets/immagine (530).png" alt=""><figcaption></figcaption></figure>

Cliccando su Crea fatture si procede alla fatturazione delle rate selezionate:

<figure><img src="../.gitbook/assets/immagine (65).png" alt=""><figcaption></figcaption></figure>

### In cosa differisce dal plugin Pianifica fatturazione?

Con questo modulo non è necessario che le righe del contratto siano già suddivise in rate, è infatti possibile impostare **liberamente** **la ricorrenza** di fatturazione, la data di inizio e l'importo di ogni rata.

Il modulo fornisce inoltre una vista generica suddivisa per mese di tutte le rate in scadenza, dalla quale è possibile **fatturare massivamente tutte le rate** tramite azione di gruppo, con la possibilità di filtrare per contratto o per cliente.

Il vero e proprio core del modulo però sta nella possibilità di configurare uno **script in cron** che provvederà alla **fatturazione automatica delle rate** secondo la configurazione stabilita, all'invio elettronico della fattura elettronica generata a CompEd (o al proprio provider di fatturazione elettronica), e all'invio di una copia di cortesia via mail al cliente.

&#x20;
