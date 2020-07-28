# Codice identificativo documento e CIG

{% hint style="info" %}
Quando si vuole emettere una fattura verso le PA è necessario riportare il **CIG** e il **Codice identificativo documento**. Come inserire questi due parametri in **OpenSTAManager**?
{% endhint %}

Il primo passo è quello di specificare nella creazione di un'anagrafica la tipologia **Ente pubblico** o **Azienda**:

![](../../.gitbook/assets/anagraficapercig.png)

Se l'anagrafica è già stata creata basta modificarla e selezionare tipologia **Ente pubblico** o **Azienda:**

![](https://github.com/devcode-it/openstamanager-docs/tree/5242b6a23c677db2f5451152c8e4c4aded3a99cf/.gitbook/assets/modifcaclienteenepubblico-1.png)

Ora, nella creazione di un **Contratto**, è possibile compilare i campi necessari per l'emissione di una Fattura verso le PA:

![](../../.gitbook/assets/datiappalto.png)

## Particolarità

I **Dati appalto** verranno visualizzati quando si aggiunge un **Contratto** ad una **fattura di vendita,** in questo modo è possibile verificare se sono stati inseriti.

![](../../.gitbook/assets/aggiuntofatturedivendita.png)

Un' ulteriore verifica della presenza o meno dei **Dati appalto** è disponibile nell'anteprima della fattura, visualizzabile tramite il pulsante **Visualizza** in **Fatturazione elettronica:**

![](../../.gitbook/assets/image%20%281%29%20%281%29.png)

![](../../.gitbook/assets/visualizzacigecodiceidentificavodocumento.png)

Infine sono visibili nel file XML generato:

![](../../.gitbook/assets/cigecodiceidentificativodocumentoxml.png)

{% hint style="info" %}
La logica precedentemente spiegata vale per l'inserimento di **Contratti, Ordini cliente** e **Interventi.**
{% endhint %}

