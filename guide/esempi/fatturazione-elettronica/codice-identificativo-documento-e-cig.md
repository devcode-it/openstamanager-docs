---
description: Guida al Codice identificativo documento e CIG in OpenSTAManager
---

# 🏷️ Codice identificativo documento e CIG

{% hint style="info" %}
Quando si vuole emettere una fattura verso le PA è necessario riportare il **CIG** e il **Codice identificativo documento**. Come inserire questi due parametri in **OpenSTAManager**?
{% endhint %}

Il primo passo è quello di specificare nella creazione di un'anagrafica la tipologia **Ente pubblico** o **Azienda**:

![](../../../.gitbook/assets/AnagraficaPerCIG.png)

Se l'anagrafica è già stata creata basta modificarla e selezionare tipologia **Ente pubblico** o **Azienda:**

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FppIgLUMrxwcgNmLNZNEW%2Ffile.png?alt=media)

Ora, nella creazione di un **Contratto**, è possibile compilare i campi necessari per l'emissione di una Fattura verso le PA:

![](../../../.gitbook/assets/DatiAppalto.png)

I **Dati appalto** verranno visualizzati quando si aggiunge un **Contratto** ad una **fattura di vendita,** in questo modo è possibile verificare se sono stati inseriti.

![](../../../.gitbook/assets/AggiuntoFattureDiVendita.png)

Un' ulteriore verifica della presenza o meno dei **Dati appalto** è disponibile nell'anteprima della fattura, visualizzabile tramite il pulsante **Visualizza** in **Fatturazione elettronica:**

![](<../../../.gitbook/assets/image (332).png>)

![](../../../.gitbook/assets/VisualizzaCIGeCodiceIdentificavoDocumento.png)

Infine sono visibili nel file XML generato:

![](../../../.gitbook/assets/CIGeCodiceIdentificativoDocumentoXML.png)

{% hint style="info" %}
La logica precedentemente spiegata vale per l'inserimento di **Contratti, Ordini cliente** e **Interventi.**
{% endhint %}
