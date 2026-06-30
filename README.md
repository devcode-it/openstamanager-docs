---
description: Elenco delle principali novità introdotte con la release 2.11.1
---

# 📣 Novità

Di seguito le principali novità della versione 2.11.1, per maggiori dettagli visitare [GitHub](https://github.com/devcode-it/openstamanager).

#### 1. Aggiornamento dipendenza protobufjs

È stata aggiornata la dipendenza `protobufjs`, libreria utilizzata per la gestione della serializzazione/deserializzazione dei dati in formato Protocol Buffers. L'aggiornamento introduce migliorie di sicurezza e compatibilità con le versioni più recenti di PHP e del runtime JavaScript.

***

#### 2. Correzioni critiche di sicurezza

È stato risolto un insieme di vulnerabilità che includevano Remote Code Execution (RCE) non autenticato via PHP Code Injection nel Configuration Wizard, SQL Injection in diversi endpoint AJAX, IDOR (Insecure Direct Object Reference) in OAuth2 e API, Reflected e Stored XSS, SSRF nella generazione PDF con mPDF e Missing Authorization sull'API delle impostazioni che permetteva la lettura e modifica di chiavi sensibili.

***

#### 3. Correzioni sulla gestione sedi e permissioni

È stata corretta la visualizzazione limitata alle sole sedi abilitate all'interno del plugin Movimenti, oltre alla gestione delle giacenze per sede in base ai permessi dell'utente. È stata inoltre sistemata la vista Articoli e la selezione seriali in fatture di vendita, garantendo una corretta segregazione dei dati per location.

***

#### 4. Correzioni funzionalità operative

Tra le principali correzioni operative: gestione dell'indirizzo di risposta nelle mail inviate, corretta impostazione dei campi CC e BCC da template email, risoluzione dell'avviso di uscita documento nei contratti, completamento automatico dati bancari, corretta creazione contratto con tipologie di attività disabilitati, eliminazione delle anagrafiche da azioni di gruppo e importazione fattura con riferimento a ordine o DDT.

***

#### 5. Correzioni UI/UX e compatibilità

Sono stati sistemati diversi problemi di interfaccia e compatibilità: corretta visualizzazione dei valori di ricerca con tema chiaro, fix del grafico delle ore interventi per tipologia (conteggia correttamente tutte le sessioni), corretta stampa riepilogo interventi, risoluzione dell'ordinamento colonne con query ORDER BY multilinea, compatibilità con PHP <= 8.5 per l'escape legacy di `fputcsv`, corretta gestione del fullcalendar nella selezione data/ora in pausa sessione e fix del tooltip informativo attività dopo trascinamento sulla dashboard.
