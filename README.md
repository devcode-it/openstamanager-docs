---
description: Elenco delle principali novità introdotte con la release 2.4.49.
---

# 📣 Novità

Di seguito le principali novità della versione 2.4.49, per maggiori dettagli visitare [GitHub](https://github.com/devcode-it/openstamanager).

➡️ Nella **Stampa scadenzario** presente in Contabilità/Stampe contabili/Scadenzario è ora possibile impostare un'anagrafica in base alla quale filtrare le scadenze da visualizzare:

<figure><img src=".gitbook/assets/immagine (639).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/immagine (641).png" alt=""><figcaption></figcaption></figure>

➡️ Aggiunta la gestione della rivalsa INPS sulla marca da bollo per il regime forfettario

➡️ Aggiunto il widget **Preventivi da fatturare**, attivabile da Strumenti/Stato dei servizi/Widget disponibili, da attivare in **Stato dei servizi**

<figure><img src=".gitbook/assets/immagine (642).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/immagine (643).png" alt=""><figcaption></figcaption></figure>

➡️ Aggiunta la gestione dell'autofattura in caso di fatture con reverse charge misto

{% hint style="warning" %}
Durante il caricamento della fattura di acquisto "estera" o in regime di reverse charge diventa ora molto importante non applicare manualmente l'IVA alle righe che non la riportano, lasciandola inserire agli automatismi in fase di creazione dell'autofattura.
{% endhint %}

{% content-ref url="guide/esempi/autofattura.md" %}
[autofattura.md](guide/esempi/autofattura.md)
{% endcontent-ref %}

➡️ In Strumenti/Impostazioni/Generali è ora possibile definire il **Tipo di sconto predefinito** da utilizzare in tutti i tipi di documenti

<figure><img src=".gitbook/assets/immagine (644).png" alt=""><figcaption></figcaption></figure>

➡️ La stampa delle fatture di vendita tra le scadenze pagamenti segna ora le rate già corrisposte:

<figure><img src=".gitbook/assets/immagine (645).png" alt=""><figcaption></figcaption></figure>

➡️ Nel modulo articoli, per gli articoli in cui è stata impostata una soglia minima, visualizza ora evidenziati in verde gli articoli presenti in quantità maggiore, e in rosso gli articoli che non rispettano questo requisito

{% hint style="warning" %}
Il filtro non evidenzia le quantità disponibili o meno, ma quelle inferiori alla soglia minima impostata nella scheda articolo nel campo **soglia minima quantità**
{% endhint %}

<figure><img src=".gitbook/assets/immagine (646).png" alt=""><figcaption></figcaption></figure>

➡️ Migliorata la struttura delle api per l'integrazione del gestionale con servizi esterni



{% content-ref url="configurazioni/introduzione/" %}
[introduzione](configurazioni/introduzione/)
{% endcontent-ref %}

➡️ Aggiunta la funzione di raggruppamento nelle righe dei preventivi:

Impostando una riga descrittiva come titolo è possibile calcolare dei subtotali

<figure><img src=".gitbook/assets/immagine (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/immagine (2).png" alt=""><figcaption></figcaption></figure>

➡️ Aggiunto link all'anteprima del documento e degli allegati in fase di invio email:

<figure><img src=".gitbook/assets/immagine (649).png" alt=""><figcaption></figcaption></figure>
