---
description: Elenco delle principali novità introdotte con la release 2.10.1
metaLinks:
  alternates:
    - https://app.gitbook.com/s/I8PynmXUVfCOtwZFC1I6/
---

# 📣 Novità

Di seguito le principali novità della versione 2.10.1, per maggiori dettagli visitare [GitHub](https://github.com/devcode-it/openstamanager).

✨ **Correzione critica di sicurezza**

Risolta la vulnerabilità di "Unauthenticated privilege escalation" che permetteva escalation di privilegi non autenticati, insieme al rafforzamento della sicurezza con prevenzione attacchi XSS e SQL injection

✨ **Ottimizzazione fatture elettroniche**

Migliorato il sistema di invio con coda di invio e campo `fe_failed_at`, con gestione automatica di tre tentativi di invio prima della rimozione dalla coda

✨ **Ottimizzazioni performance**

Miglioramento delle query con Laravel, ottimizzazione del plugin consuntivo e delle classi documenti con generazione più efficiente del numero progressivo

✨ **Correzioni calcoli orari**

Risolto il conteggio ore in header e il calcolo delle ore totali dei contratti che non venivano sommate correttamente

✨ **Miglioramenti interfaccia utente**

Migliorata la modale di aggiunta articolo, il grafico header interventi e i tasti azione sulle righe, con supporto alla copia righe anche per documenti bloccati

✨ **Correzioni funzionalità documenti**

Risolti problemi nella visualizzazione documenti collegati a contratti, nella generazione fatture elettroniche per sedi committente paesi esteri e nella gestione della modifica IVA massiva

