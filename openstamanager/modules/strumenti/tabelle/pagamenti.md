---
description: Come gestire i pagamenti in OpenSTAManager
---

# 💶 Pagamenti

{% hint style="info" %}
Il modulo **Pagamenti** permette di creare e modificare i pagamenti presenti nel gestionale.
{% endhint %}

![](<../../../../.gitbook/assets/image (204).png>)

## ➕ Creazione

Per creare un nuovo tipo di pagamento si dovrà cliccare sul tasto (+).

Andranno qui inseriti la descrizione e il codice modalità (fatturazione elettronica) del nuovo tipo di pagamento.

![](<../../../../.gitbook/assets/image (192).png>)

## 🖌️ Modifica

Cliccando sul record da modificare si aprirà la schermata di dettaglio, da cui sarà possibile modificare:

* Descrizione
* Codice modalità (fatturazione elettronica)
* Conto predefinito per le vendite
* Conto predefinito per gli acquisti
* Rate
  * Percentuale
  * Scadenza
  * Giorno
  * Distanza in giorni

![](<../../../../.gitbook/assets/image (224).png>)

#### ESEMPI:

Volendo aggiungere alle modalità di pagamento il Bonifico 60/90/120gg d.f.f.m si dovrà aggiungere un nuovo tipo di pagamento che riporterà 3 rate da 33%, 33% e 34% dell'importo complessivo, rispettivamente a 60, 90 e 120 giorni dalla data di emissione della fattura (Da specificare nel campo **Distanza in giorni**).

Nel campo scadenza andrà riportato "Data fatturazione fine mese", così la data della scadenza generata verrà impostata alla fine del mese in cui cadrebbe la data calcolata in base alla **Distanza in giorni** impostata.

<figure><img src="../../../../.gitbook/assets/pagamenti (1).png" alt=""><figcaption></figcaption></figure>

Selezionando questa modalità di pagamento in una fattura di vendita verranno quindi generate tre scadenze:

<figure><img src="../../../../.gitbook/assets/immagine.png" alt=""><figcaption></figcaption></figure>
