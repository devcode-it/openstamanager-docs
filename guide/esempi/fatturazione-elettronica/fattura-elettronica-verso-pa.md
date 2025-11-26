---
description: Come emettere fattura elettronica verso una Pubblica Amministrazione
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/LFXMzl7lx1tPtA15nWw7/guide/esempi/fatturazione-elettronica/fattura-elettronica-verso-pa
---

# 🏫 Fattura elettronica verso PA

Per emettere una fattura elettronica nei confronti di una Pubblica Amministrazione come prima cosa si dovrà verificare di aver registrato correttamente la relativa anagrafica.

Nello specifico essa deve riportare come Tipologia la voce "Ente pubblico" e deve essere stato specificato il corretto Codice destinatario.

<figure><img src="../../../.gitbook/assets/immagine (724).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
I codici destinatario degli enti pubblici sono composti da 6 caratteri che indentificano ogni ente pubblico e sono censiti e consultabili nel sito [https://www.indicepa.gov.it/ipa-portale/](https://www.indicepa.gov.it/ipa-portale/)
{% endhint %}

Dopo aver registrato correttamente l'anagrafica si dovrà procedere ad emettere fattura da Vendite/Fatture di vendita cliccando sul tasto (+).

Si dovrà qui selezionare l'Ente pubblico e cliccare su Aggiungi.

<figure><img src="../../../.gitbook/assets/immagine (655).png" alt=""><figcaption></figcaption></figure>

Si potrà ora procedere al completamento dei dati da riportare in fattura inserendo le righe e andando ad attivare l'impostazione "Split payment", un meccanismo secondo cui la PA acquirente non corrisponde l'IVA presente in fattura al fornitore ma la trattiene e la versa direttamente all'erario.

&#x20;                                          <img src="../../../.gitbook/assets/immagine (582).png" alt="" data-size="original">



Devono seguire le regole dello Split Payment **tutti coloro che emettono fatture alla PA**, tranne:

* i professionisti con ritenuta alla fonte a titolo d'acconto o di imposta sul reddito,
* i Contribuenti Forfettari e i soggetti a regimi speciali IVA.

Si dovrà ora cliccare su Attributi avanzati.

<figure><img src="../../../.gitbook/assets/immagine (723).png" alt=""><figcaption></figcaption></figure>

Le fatture elettroniche emesse verso le PA infatti, dovranno riportare obbligatoriamente:

* il codice identificativo di gara (CIG), composto da 10 caratteri alfanumerici che serve a identificare una gara d'appalto.
* il codice unico di progetto (CUP), composto da 15 caratteri alfanumerici che identifica un progetto d'investimento pubblico.

Le amministrazioni non potranno procedere al pagamento delle fatture elettroniche che non riportano i codici CIG e CUP, quest'ultimo ove previsto.

Questi codici vanno inseriti nelle voci 2.1.2.6 CodiceCUP e 2.1.2.7 CodiceCIG **dopo aver specificato il corretto 2.1.2.2 IdDocumento.**

<figure><img src="../../../.gitbook/assets/immagine (917).png" alt=""><figcaption></figcaption></figure>

Sarà ora possibile emettere e inviare elettronicamente la fattura appena generata.

Quando la fattura verrà elaborata dallo SDI e si andrà a importare la ricevuta nel gestionale, essa potrà poi riportare diversi stati:

* **Scartata:** la fattura non ha superato i controlli dello SDI, si dovranno apportare le opportune correzioni e procedere a reinviare il documento entro 5 giorni dalla ricezione della notifica;
* **Mancata consegna:** la fattura non è stata recapitata alla PA;
* **Avvenuta trasmissione:** il recapito alla PA non è andato a buon fine, si può chiedere alla PA il controllo del documento e l'eventuale liquidazione dello stesso;
* **Consegnata:** la fattura ha superato i controlli dello SDI e il recapito alla PA è andato a buon fine;
* **Accettata:** La PA ha accettato la fattura;
* **Rifiutata:** La PA ha rifiutato la fattura. Si dovrà emettere nota di credito per stornarla e creare una nuova fattura.
* **Decorrenza termini:** se la PA ha ricevuto la fattura, ma nei 15 giorni successivi non ha segnalato nessun esito, verrà recapitata la notifica di decorrenza termini. Questa notifica non determina la correttezza della fattura, nè come verrà gestita successivamente dalla PA. **Essa verrà automaticamente considerata come Accettata.**
