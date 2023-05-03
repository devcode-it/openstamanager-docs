---
description: Elenco delle principali novità introdotte con la release 2.4.45.
---

# 📣 Novità

Di seguito le principali novità della versione 2.4.45, per maggiori dettagli visitare [GitHub](https://github.com/devcode-it/openstamanager).

➡️  Aggiunta la gestione dell'unità di misura secondaria in fase di [importazione di una fattura elettronica](openstamanager/modules/acquisti/fatturediacquisto/fatturazione-elettronica.md):

<figure><img src=".gitbook/assets/immagine (25).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/immagine (5).png" alt=""><figcaption></figcaption></figure>

➡️  Migliorati i filtri uguale e diverso nelle tabelle

La ricerca con l'operatore **=** (uguale) e **!=** (diverso) ora restituisce come risultato tutti i record che contengono le parole ricercate.

Ad esempio volendo cercare tutti gli articoli che contengono esattamente '540' nella descrizione, sarà sufficiente digitare =540

<figure><img src=".gitbook/assets/immagine (4).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/immagine (29).png" alt=""><figcaption></figcaption></figure>

Al contrario, volendo selezionare tutti gli articoli che non contengono esattamente '540', sarà sufficiente digitare !=540

<figure><img src=".gitbook/assets/immagine (31).png" alt=""><figcaption></figcaption></figure>

➡️ Aggiunta la funzione **Confronta prezzi** nei documenti

Correzioni:

➡️  Corretta l'impostazione del prezzo articolo da listino in contratti e preventivi

➡️  Corretta l'impostazione agente in creazione documento

➡️  Corrette le query nelle viste Attività, Ordini clienti, Ordini fornitori e Preventivi.
