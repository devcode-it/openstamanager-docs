# Codice identificativo documento e CIG

{% hint style="info" %}
Quando si vuole emettere una fattura verso le PA è necessario riportare il **CIG** e il **Codice identificativo documento**. Come inserire questi due parametri in **OpenSTAManager**?
{% endhint %}

Il primo passo è quello di specificare nella creazione di un'anagrafica **Cliente** la tipologia **Ente pubblico**:

![](../../../.gitbook/assets/anagraficapercig%20%281%29.png)

Se l'anagrafica è già stata creata basta modificarla e selezionare tipologia **Ente pubblico:**

![](../../../.gitbook/assets/modifcaclienteenepubblico.png)

Ora, nella creazione di un **Contratto**, è possibile compilare i campi necessari per l'emissione di una Fattura verso le PA:

![](../../../.gitbook/assets/datiappalto.png)

### Particolarità

I **Dati appalto** verranno visualizzati quando si aggiunge un **Contratto** ad una **fattura di vendita,** in questo modo è possibile verificare se sono stati inseriti. 

![](../../../.gitbook/assets/aggiuntofatturedivendita.png)

Un' ulteriore verifica della presenza o meno dei **Dati appalto** è presente nell'anteprima della fattura cliccando su **Visualizza** in **Fatturazione elettronica:**

![](../../../.gitbook/assets/visualizzafe%20%281%29.png)

![](../../../.gitbook/assets/visualizzacigecodiceidentificavodocumento.png)

Infine sono visibili nel file XML generato:

![](../../../.gitbook/assets/cigecodiceidentificativodocumentoxml.png)

{% hint style="warning" %}
La logica precedentemente spiegata non vale solo nell'inserimento di un **Contratto** ma anche per **Ordine cliente** e **Interventi**
{% endhint %}

\*\*\*\*

