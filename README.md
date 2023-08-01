---
description: Elenco delle principali novità introdotte con la release 2.4.48.
---

# 📣 Novità

Di seguito le principali novità della versione 2.4.48, per maggiori dettagli visitare [GitHub](https://github.com/devcode-it/openstamanager).

➡️ Aggiunta la gestione della firma con **tavoletta grafica**

E' ora possibile configurare una tavoletta grafica Wacom da utilizzare per la firma dei documenti. I requisiti per l'utilizzo della tavoletta grafica sono:

* i browser supportati sono: Chrome, Edge e Opera
* la connessione deve essere sicura (https)
* la configurazione è stata eseguita con la tavoletta **Wacom Signature STU540**

maggiori informazioni: [https://openstamanager.com/blog/tavoletta-grafica/](https://openstamanager.com/blog/tavoletta-grafica/)

➡️ E' ora possibile modificare gli stati predefiniti per gli ordini clienti e fornitori dal nuovo modulo **Stati degli ordini** raggiungibile in Strumenti/**Stati degli ordini**.

<figure><img src=".gitbook/assets/immagine (601).png" alt=""><figcaption></figcaption></figure>

➡️ E' stata migliorata la gestione dei filtri per data nelle tabelle. E' ora possibile filtrare per > o < una determinata data:

<figure><img src=".gitbook/assets/immagine (602).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/immagine (603).png" alt=""><figcaption></figcaption></figure>

➡️ E' stato aggiunto un controllo sulle fatture di vendita, che blocca l'emissione del documento e visualizza un avviso nel caso sia presente un altro documento con lo stesso numero e anno della fattura che si sta provando a emettere.

➡️ I numero di log massimi conservati a gestionale sono ora limitati a 30 file.

➡️ Migliorata la gestione delle **checklist**, è possibile ora definire una voce come titolo e la sua gestione avviene attraverso ckeditor (è quindi possibile inserire tabelle, emoticon, immagini e applicare stili al testo).

➡️ Sono stati ripristinati gli automatismi relativi ai piani di sconto, non più applicati dalla versione 2.4.40 a causa della nuova gestione delle righe.

➡️  Corretta la gestione degli arrotondamenti in fase di importazione fatture elettroniche, sono ora supportati anche casi particolari di arrotodamenti applicati sull'imponibile.

➡️ Corretto l'errore che inseriva un campo A: per ogni valore inserito in fase di invio mail.
