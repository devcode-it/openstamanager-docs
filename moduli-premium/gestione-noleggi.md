---
description: Guida al modulo Gestione noleggi in OpenSTAMAanager
---

# 📗 Gestione noleggi

Il modulo **Gestione Noleggi** è un'estensione per **OpenSTAManager** che permette di gestire in modo completo e integrato il noleggio di impianti e attrezzature. Il modulo offre funzionalità avanzate per tracciare lo stato dei noleggi, associare contratti e clienti, e mantenere uno storico dettagliato di tutte le operazioni.

<figure><img src="../.gitbook/assets/immagine (5).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/immagine (4).png" alt=""><figcaption></figcaption></figure>

### Caratteristiche Principali

#### Gestione Noleggi

* **Creazione e modifica noleggi**: Registrazione completa di nuovi noleggi con tutte le informazioni necessarie
* **Tracciamento stato**: Monitoraggio dello stato del noleggio (in corso, concluso, annullato, sospeso)
* **Gestione date**: Controllo preciso delle date di inizio, fine e riconsegna
* **Associazione clienti**: Collegamento diretto con le anagrafiche clienti
* **Contratti di noleggio**: Possibilità di associare contratti ai noleggi
* **Ubicazione**: Tracciamento del luogo dove viene utilizzato l'impianto
* **Note aggiuntive**: Campo per annotazioni e dettagli specifici

#### Gestione Stati Noleggio

* **Stati personalizzabili**: Creazione e modifica degli stati dei noleggi
* **Codici univoci**: Assegnazione di codici identificativi per ogni stato
* **Colori personalizzati**: Assegnazione di colori per una visualizzazione immediata
* **Flag di disponibilità**: Indicazione se lo stato rende l'impianto disponibile per nuovi noleggi

#### Interfaccia Utente

* **Dashboard intuitiva**: Visualizzazione chiara delle informazioni dell'impianto
* **Storico completo**: Tabella dettagliata di tutti i noleggi effettuati
* **Indicatore di disponibilità**: Badge visivo per identificare rapidamente se l'impianto è disponibile
* **Avvisi di scadenza**: Evidenziazione automatica dei noleggi scaduti
* **Azioni rapide**: Pulsanti per modificare, eliminare e registrare riconsegne

#### Stati Predefiniti

Il modulo viene fornito con i seguenti stati predefiniti:

| Codice | Descrizione | Colore           | Noleggiabile |
| ------ | ----------- | ---------------- | ------------ |
| INC    | In corso    | Verde (success)  | No           |
| CON    | Concluso    | Blu (info)       | Sì           |
| ANN    | Annullato   | Rosso (danger)   | Sì           |
| SOS    | Sospeso     | Giallo (warning) | No           |

#### Personalizzazione

È possibile aggiungere, modificare o eliminare stati dal menu **Tabelle → Stati noleggio**.

### Guida all'Uso

#### Visualizzazione Noleggi

1. Accedere al modulo **Gestione noleggi** dal menu principale
2. Selezionare un impianto dalla lista per visualizzare i dettagli
3. La scheda mostra:
   * **Dettagli Impianto**: Informazioni complete sull'impianto con indicatore di disponibilità
   * **Cliente Attuale**: Dati del cliente associato all'ultimo noleggio
   * **Storico Noleggi**: Tabella completa di tutti i noleggi effettuati

#### Creazione di un Nuovo Noleggio

1. Dalla scheda dell'impianto, cliccare sul pulsante **"Nuovo Noleggio"** (disponibile solo se l'impianto è disponibile)
2. Compilare il form con le seguenti informazioni:
   * **Periodo**: Selezionare le date di inizio e fine tramite il date range picker
   * **Cliente**: Selezionare l'anagrafica cliente dal database
   * **Contratto**: (Opzionale) Associare un contratto esistente
   * **Stato**: Selezionare lo stato iniziale del noleggio
   * **Ubicazione**: Indicare il luogo di utilizzo
   * **Note**: Aggiungere eventuali annotazioni
3. Cliccare su **"Aggiungi"** per confermare



#### Modifica di un Noleggio Esistente

1. Dalla tabella **Storico Noleggi**, individuare il noleggio da modificare
2. Cliccare sull'icona **modifica** (penna)
3. Modificare i campi desiderati
4. Salvare le modifiche

#### Registrazione della Riconsegna

1. Dalla tabella **Storico Noleggi**, individuare un noleggio "In corso"
2. Cliccare sull'icona **riconsegna** (freccia indietro)
3. Selezionare la data di riconsegna nel calendario
4. Confermare l'operazione
5. Lo stato del noleggio passerà automaticamente a "Concluso"

#### Eliminazione di un Noleggio

⚠️ **Nota**: L'eliminazione è disponibile solo per gli utenti con permessi di amministratore.

1. Dalla tabella **Storico Noleggi**, individuare il noleggio da eliminare
2. Cliccare sull'icona **elimina** (cestino)
3. Confermare l'operazione

#### Gestione degli Stati

**Aggiungere un Nuovo Stato**

1. Accedere a **Tabelle → Stati noleggio**
2. Cliccare su **"Aggiungi"**
3. Inserire:
   * **Codice**: Codice breve identificativo (max 10 caratteri)
   * **Descrizione**: Nome descrittivo dello stato
   * **Colore**: Selezionare il colore per la visualizzazione
4. Cliccare su **"Aggiungi"** per confermare

**Modificare uno Stato Esistente**

1. Accedere a **Tabelle → Stati noleggio**
2. Selezionare lo stato da modificare
3. Modificare i campi desiderati
4. Impostare il flag **"Disponibile per il noleggio"** se necessario
5. Salvare le modifiche

**Eliminare uno Stato**

⚠️ **Nota**: Se lo stato è stato utilizzato in almeno un noleggio, verrà effettuato un soft-delete. Se non è mai stato utilizzato, verrà eliminato definitivamente.

1. Accedere a **Tabelle → Stati noleggio**
2. Selezionare lo stato da eliminare
3. Cliccare su **"Elimina"**
4. Confermare l'operazione

### Funzionalità Avanzate

#### Date Range Picker

Il modulo utilizza un date range picker avanzato che offre:

* Selezione rapida di periodi predefiniti (Oggi, Domani, Prossimi 7 giorni, ecc.)
* Selezione personalizzata tramite calendari interattivi
* Localizzazione in italiano
* Calendari collegati per facilitare la selezione

#### Indicatore di Disponibilità

L'impianto mostra un badge colorato:

* 🟢 **Verde**: Disponibile per nuovi noleggi
* 🔴 **Rosso**: Attualmente noleggiato

Il pulsante "Nuovo Noleggio" è disabilitato quando l'impianto non è disponibile.

#### Avvisi di Scadenza

I noleggi con data fine precedente alla data corrente e stato "In corso" vengono evidenziati con:

* Sfondo giallo nella tabella
* Icona di avviso
* Testo "Scaduto" in rosso

### Personalizzazione

#### Modifica dei Colori

I colori degli stati possono essere personalizzati modificando il campo `colore` nella tabella `st_stati_noleggi`. I colori sono espressi in formato esadecimale (es. `#ff0000`).

***

## Changelog

Tutti i maggiori cambiamenti di questo progetto saranno documentati in questo file. Per informazioni più dettagliate, consultare il log GIT della repository su GitHub.

Il formato utilizzato è basato sulle linee guida di [Keep a Changelog](http://keepachangelog.com/), e il progetto segue il [Semantic Versioning](http://semver.org/) per definire le versioni delle release.

* 4.0 (2026-03-19)
* 3.0 (2025-07-24)
* 2.0 (2025-05-21)
* 1.0 (2025-04-09)

### 4.0 (2026-03-19)

#### Aggiunto (Added)

* Aggiunti i file JSON di controllo del modulo: `modules.json`, `mysql.json`, `settings.json`, `views.json` e `widgets.json`
* Documentazione completa del modulo con README dettagliato

### 3.0 (2025-07-24)

#### Modificato (Changed)

* Migliorata la grafica del modulo noleggi
* Aggiornate le schermate e i flussi di gestione dei noleggi

### 2.0 (2025-05-21)

#### Modificato (Changed)

* Allineato il modulo alla versione 2.8

### 1.0 (2025-04-09)

#### Corretto (Fixed)

* Applicate correzioni minori alla prima release del modulo
