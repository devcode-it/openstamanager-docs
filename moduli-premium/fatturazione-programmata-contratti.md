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

Il nuovo contratto deve riportare una data di accettazione e di conclusione, ed essere in stato **In lavorazione**.

Per pianificare la fatturazione è sufficiente accedere al plugin **Ricorrenza fatturazione:**

<figure><img src="../.gitbook/assets/immagine (1022).png" alt=""><figcaption></figcaption></figure>

Da qui sarà possibile definire la ricorrenza di fatturazione, la data di inizio e l'importo che dovrà avere ogni rata. Al salvataggio delle impostazioni verrà visualizzata una tabella con tutte le scadenze generate:

<figure><img src="../.gitbook/assets/immagine (1024).png" alt=""><figcaption></figcaption></figure>

Sarà ora possibile visualizzare le rate da fatturare dal modulo **Fatturazione contratti,** filtrate in base al mese in corso.

<figure><img src="../.gitbook/assets/immagine (1025).png" alt=""><figcaption></figcaption></figure>

Volendo fatturare le rate manualmente, sarà sufficiente selezionare le rate interessate e cliccare su Crea fattura. Da qui sarà possibile selezionare se accodare le rate selezionate a fatture della stessa anagrafica in stato Bozza, e modificare la data, il sezionale e il tipo di fattura.

<figure><img src="../.gitbook/assets/immagine (1026).png" alt=""><figcaption></figcaption></figure>

Cliccando su Crea fatture si procede alla fatturazione delle rate selezionate:

<figure><img src="../.gitbook/assets/immagine (1027).png" alt=""><figcaption></figcaption></figure>

Tornando al contratto e navigando al plugin Ricorrenza fatturazione è ora possibile visualizzare la rata appena fatturata.

<figure><img src="../.gitbook/assets/immagine (1028).png" alt=""><figcaption></figcaption></figure>

### Configurazione

All'installazione del modulo in Strumenti/Impostazioni nella sezione Contratti sarà possibile trovare le seguenti impostazioni:

<figure><img src="../.gitbook/assets/immagine (944).png" alt=""><figcaption></figcaption></figure>

* **Descrizione righe nella fatturazione dei contratti:** E' qui possibile definire il formato che avranno le righe della fattura generata tramite automatismo.
* **Cron fatturazione:** E' qui possibile scegliere gli automatismi da eseguire, scegliendo tra: emissione della fattura, emissione della fattura e invio di copia di cortesia via email, ed emissione della fattura, invio di copia di cortesia via email e invio dell'xml allo SDI.
* **Elaborazione invio automatico XML:** In questa impostazione è possibile definire i giorni di ritardo dall'emissione dell'XML al suo invio allo SDI, per permettere la sua eventuale modifica. Se al documento venisse variato lo stato entro i giorni stabiliti, l'automatismo viene interrotto e occorrerà inviare il file manualmente.

### In cosa differisce dal plugin Pianifica fatturazione?

Con questo modulo non è necessario che le righe del contratto siano già suddivise in rate, è infatti possibile impostare **liberamente** **la ricorrenza** di fatturazione, la data di inizio e l'importo di ogni rata.

Il modulo fornisce inoltre una vista generica suddivisa per mese di tutte le rate in scadenza, dalla quale è possibile **fatturare massivamente tutte le rate** tramite azione di gruppo, con la possibilità di filtrare per contratto o per cliente.

Il vero e proprio core del modulo però sta nella possibilità di configurare uno **script in cron** che provvederà alla **fatturazione automatica delle rate** secondo la configurazione stabilita, all'invio elettronico della fattura elettronica generata a CompEd (o al proprio provider di fatturazione elettronica), e all'invio di una copia di cortesia via mail al cliente.

&#x20;
