---
description: Elenco delle principali novità introdotte con la release 2.10.2
metaLinks:
  alternates:
    - https://app.gitbook.com/s/WzoKFijlVGKTMgti0acZ/
---

# 📣 Novità

Di seguito le principali novità della versione 2.10.2, per maggiori dettagli visitare [GitHub](https://github.com/devcode-it/openstamanager).

### 🔒 Correzioni di Sicurezza

* **Remote Code Execution via Insecure Deserialization in OAuth2** - Vulnerabilità critica risolta
* **Time-Based Blind SQL Injection** tramite parametro `options[stato]`
* **SQL Injection** tramite parametro `righe` nei modali di confronto righe
* **SQL Injection** nel modulo Aggiornamenti
* **SQL Injection** - Corrette vulnerabilità attraverso l'utilizzo della funzione `prepare()` per l'escaping delle variabili nelle query SQL

### 🐛 Bugfix

#### Fatturazione elettronica e documenti

* Generazione fatture con righe descrittive da azioni di gruppo
* Creazione ordine fornitore da preventivo per righe descrittive
* Blocco campi numero e data per fatture elettroniche importate
* Pagamenti automatici in importazione FE
* Movimento automatico di rilevazione IVA

#### Gestione seriali e progressivi

* Evasione seriali nel caso di seriali senza documento di acquisto associato
* Generazione progressivo per maschere senza riferimento all'anno

#### Contabilità e movimenti

* Generazione moviment**i** applicando correttamente la data registrazione fattura

#### Installazione e moduli

* Redirect in aggiornamento che impediva la corretta installazione dei moduli risolto
