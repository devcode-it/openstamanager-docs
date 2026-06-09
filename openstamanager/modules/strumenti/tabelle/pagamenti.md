---
description: Come gestire i pagamenti in OpenSTAManager
icon: circle
---

# Pagamenti

{% hint style="info" %}
Il modulo **Pagamenti** permette di creare e modificare i pagamenti presenti nel gestionale.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (889).png" alt=""><figcaption></figcaption></figure>

## Creazione

Per creare un nuovo tipo di pagamento si dovrà cliccare sul tasto (+).

Andranno qui inseriti la descrizione e il codice modalità (fatturazione elettronica) del nuovo tipo di pagamento.

<figure><img src="../../../../.gitbook/assets/image (890).png" alt=""><figcaption></figcaption></figure>

## Modifica

Cliccando sul record da modificare si aprirà la schermata di dettaglio, da cui sarà possibile modificare:

* Descrizione
* Codice modalità (fatturazione elettronica)
* Conto predefinito per le vendite
* Conto predefinito per gli acquisti
* Descrizione riga
* Importo fisso
* Importo percentuale
* Rate
  * Percentuale
  * Scadenza
  * Giorno
  * Distanza in giorni

<figure><img src="../../../../.gitbook/assets/image (891).png" alt=""><figcaption></figcaption></figure>

#### ESEMPI:

Volendo aggiungere alle modalità di pagamento il **Bonifico 30/60/90gg d.f.f.m** si dovrà aggiungere un nuovo tipo di pagamento che riporterà 3 rate da 33%, 33% e 34% dell'importo complessivo, rispettivamente a 30, 60 e 90 giorni dalla data di emissione della fattura (da specificare nel campo **Distanza in giorni**).

Nel campo scadenza andrà riportato "Data fatturazione fine mese", così la data della scadenza generata verrà impostata alla fine del mese in cui cadrebbe la data calcolata in base alla **Distanza in giorni** impostata.

<figure><img src="../../../../.gitbook/assets/image (892).png" alt=""><figcaption></figcaption></figure>

Selezionando questa modalità di pagamento in una fattura di vendita con data 10/02/2023  verranno quindi generate tre scadenze:

<figure><img src="../../../../.gitbook/assets/immagine (495).png" alt=""><figcaption></figcaption></figure>

Volendo aggiungere alle modalità di pagamento il **Bonifico 30gg d.f.f.m + 10** si dovrà aggiungere un nuovo tipo di pagamento che riporterà una rata del 100% dell'importo complessivo, a 30 giorni dalla data di emissione della fattura (da specificare nel campo **Distanza in giorni**).

Nel campo scadenza andrà riportato "Data fatturazione fine mese (giorno fisso)", così la data della scadenza generata verrà impostata alla fine del mese in cui cadrebbe la data calcolata in base alla **Distanza in giorni** impostata.

<figure><img src="../../../../.gitbook/assets/immagine (834).png" alt=""><figcaption></figcaption></figure>

Selezionando questa modalità di pagamento in una fattura di vendita con data 10/02/2023 verrà quindi generata la seguente scadenza:

<figure><img src="../../../../.gitbook/assets/immagine (494).png" alt=""><figcaption></figcaption></figure>
