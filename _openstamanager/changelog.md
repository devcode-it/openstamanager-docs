---
title: OpenSTAManager 2.4.2
permalink: /openstamanager/2.4.2/
sidebar:
    nav: none
---

### Aggiunto (Added)

 - Plugin per la Fatturazione Elettronica
 - Libreria autonoma per i messaggi da mostrare all'utente
 - Logging completo delle azioni degli utente (accessibile agli Amministratori)
 - Supporto a [Prepared Statements PDO](http://php.net/manual/it/pdo.prepared-statements.php)
 - Impostazioni da definire durante l'installazione e l'aggiornamento del software
 - Helper per semplificare lo sviluppo di codice indipendente (file `lib/helpers.php`)
 - Funzioni generiche per moduli e plugin (file `lib/common.php`)
 - API per la gestione dell'applicazione

### Modificato (Changed)

- Normalizzazione delle nazioni registrate dal gestionale (https://github.com/umpirsky/country-list)
- Miglioramenti nella gestione dei record (variabile `$record` al posto di `$records[0]`)
- Ottimizzazione delle query di conteggio (metodo `fetchNum`)
- Aggiungere un tecnico in un Intervento salva le modifiche apportate in precedenza

### Deprecato (Deprecated)

- Variabili globali $post e $get, da sostituire con le funzioni `post()` e `get()`
- Funzione `get_var()`, da sostituire con la funzione `setting()`
- Funzioni PHP inutilizzate: `datediff()`, `unique_filename()`, `create_thumbnails()`

### Rimosso (Removed)

- Funzioni PHP deprecate nella versione 2.3.*

### Sicurezza (Security)

- Abilitata protezione contro attacchi CSRF
