---
description: Guida alla registrazione ed evasioni degli ordini in OpenSTAManager
---

# 📦 Evasione ordine

### 📕 Registrare un ordine cliente

{% content-ref url="../../openstamanager/modules/vendite/ordinicliente/" %}
[ordinicliente](../../openstamanager/modules/vendite/ordinicliente/)
{% endcontent-ref %}

### 📕 Creazione DDT di vendita

Dall'ordine cliente appena registrato è possibile cliccare su Crea/Ddt per creare un DDT di vendita.

<figure><img src="../../.gitbook/assets/immagine (632).png" alt=""><figcaption></figcaption></figure>

Per creare un DDT da più ordini cliente invece sarà sufficiente accedere al modulo **Magazzino/Spedizione ordini**, selezionare gli ordini interessari e cliccare su **Azioni di gruppo/Crea DDT**.

<figure><img src="../../.gitbook/assets/immagine (117).png" alt=""><figcaption></figcaption></figure>

Verrà così creato un DDT che riporterà le righe da evadere con quantità disponibili a magazzino degli ordini cliente, non verranno quindi riportati gli articoli con quantità insufficiente.

<figure><img src="../../.gitbook/assets/immagine (643).png" alt=""><figcaption></figcaption></figure>

### 📕 Fatturazione del DDT di vendita

A seguito dell'evasione dei DDT di vendita sarà possibile procedere alla loro fatturazione massiva tramite **Azioni di gruppo/Fattura DDT di vendita**.&#x20;

<figure><img src="../../.gitbook/assets/immagine (636).png" alt=""><figcaption></figcaption></figure>

Verrà così creata una fattura di vendita che riporterà gli articoli presenti nelle righe dei DDT, con i rispettivi riferimenti ai DDT originali:

<figure><img src="../../.gitbook/assets/immagine (631).png" alt=""><figcaption></figcaption></figure>

### 📕 Registrazione del pagamento della fattura

A seguito dell'emissione della fattura di vendita verrà creata la rispettiva scadenza a scadenzario. E' possibile registrare il pagamento del pagamento dalla fattura tramite l'apposito tasto **Registra contabile**, o tramite il pulsante in corrispondenza alla scadenza.

<figure><img src="../../.gitbook/assets/immagine (639).png" alt=""><figcaption></figcaption></figure>

Cliccando su Aggiungi verrà così registrato in prima nota il movimento relativo al pagamento della fattura, e la rispettiva scadenza verrà chiusa.

<figure><img src="../../.gitbook/assets/immagine (640).png" alt=""><figcaption></figcaption></figure>

Sarà ora possibile visualizzare il cambio di stato automatico in **Pagato** della fattura, dal modulo **Fatture di vendita**.

<figure><img src="../../.gitbook/assets/immagine (637).png" alt=""><figcaption></figcaption></figure>