---
description: Elenco delle principali novità introdotte con la release 2.4.45.
---

# 📣 Novità

Di seguito le principali novità della versione 2.4.45, per maggiori dettagli visitare [GitHub](https://github.com/devcode-it/openstamanager).

➡️  In fase di [importazione di una fattura elettronica](openstamanager/modules/acquisti/fatturediacquisto/fatturazione-elettronica.md) è ora possibile convertire le quantità di un articolo da un unità di misura ad un'altra, ad esempio registrando una fattura di un fornitore che vende 100kg di materiale è possibile caricare in magazzino l'equivalente in metri piuttosto che litri, effettuando quindi la conversione automatica.

<figure><img src=".gitbook/assets/immagine (25) (2).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/immagine (5) (4) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;➡️ Aggiunta la possibilità di [importare i **Preventivi**](guide/esempi/import-preventivi.md) da un file CSV

<figure><img src=".gitbook/assets/immagine (8) (1).png" alt=""><figcaption></figcaption></figure>

➡️  Migliorati i filtri uguale e diverso nelle [tabelle](https://docs.openstamanager.com/v/2.4.45/openstamanager/interfaccia/moduli-e-plugin#tabella-generale)

La ricerca con l'operatore **=** (uguale) e **!=** (diverso) ora restituisce come risultato tutti i record che contengono le parole ricercate.

Ad esempio volendo cercare tutti gli articoli che contengono esattamente '540' nella descrizione, sarà sufficiente digitare =540

<figure><img src=".gitbook/assets/immagine (4).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/immagine (29).png" alt=""><figcaption></figcaption></figure>

Al contrario, volendo selezionare tutti gli articoli che non contengono esattamente '540', sarà sufficiente digitare !=540

<figure><img src=".gitbook/assets/immagine (31).png" alt=""><figcaption></figcaption></figure>

➡️ Aggiunta la funzione [**Confronta prezzi**](https://docs.openstamanager.com/v/2.4.45/openstamanager/modules/vendite/fatturedivendita#confronta-prezzi) nei documenti

E' ora possibile selezionare le righe corrispondenti agli articoli nei documenti e confrontarne e modificarne massivamente il prezzo di vendita e di acquisto.

<figure><img src=".gitbook/assets/immagine (26).png" alt=""><figcaption></figcaption></figure>
