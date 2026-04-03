---
description: Elenco delle principali novità introdotte con la release 2.10.3
metaLinks:
  alternates:
    - https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/
---

# 📣 Novità

Di seguito le principali novità della versione 2.10.3, per maggiori dettagli visitare [GitHub](https://github.com/devcode-it/openstamanager).

### 1. **Miglioramenti alla contabilità e fatturazione**

La release 2.10.3 introduce importanti correzioni nel modulo contabilità, risolvendo problemi critici come la registrazione degli insoluti, le scritture contabili quando si riapre un documento e la generazione corretta dei movimenti delle autofatture durante l'importazione delle fatture elettroniche. Sono stati inoltre corretti l'emissione delle fatture con data automatica e l'addebito delle spese di incasso per fatture non in bozza.

### 2. **Ottimizzazione della gestione log di sistema**

È stata migliorata la gestione dei log di Laravel, che ora vengono salvati in `logs/app.log` con una rotazione giornaliera automatica a 30 giorni. Questa ottimizzazione garantisce una migliore organizzazione dei file di log e un utilizzo più efficiente dello spazio su disco.

### 3. **Migliorie alla stampa riepilogo interventi**

La stampa del riepilogo interventi è stata migliorata graficamente con l'introduzione di tabelle di riepilogo più chiare per le sessioni di lavoro e il materiale utilizzato, rendendo i documenti più professionali e facili da consultare.

### 4. **Ottimizzazione esportazione calendario**

Il formato di esportazione ICS per il calendario è stato ottimizzato, permettendo una migliore integrazione con i principali calendari esterni e applicazioni di gestione appuntamenti.

### 5. **Correzioni nell'area statistiche e dashboard**

Sono stati risolti problemi nel grafico vendite e acquisti del modulo Statistiche e migliorato il tooltip delle sessioni nella dashboard, che ora visualizza correttamente solo la sessione selezionata, offrendo un'esperienza utente più fluida e precisa.
