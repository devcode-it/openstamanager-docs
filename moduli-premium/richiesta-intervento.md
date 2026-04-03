---
description: Guida al modulo aggiuntivo Richiesta intervento in OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/moduli-premium/richiesta-intervento
---

# 📗 Richiesta intervento

{% hint style="info" %}
Il modulo **Richiesta intervento** permette l'apertura di richieste di intervento (ticket) all'interno del gestionale.
{% endhint %}

Il modulo Richiesta intervento è un componente aggiuntivo di OpenSTAManager che consente ai clienti di inviare richieste di assistenza tecnica in modo semplice e diretto. Le richieste vengono gestite come ticket all'interno del sistema, permettendo un'efficiente organizzazione e tracciabilità delle attività di supporto.

#### Caratteristiche principali

* 📝 Form di richiesta intuitivo e accessibile
* 👤 Accesso con registrazione o come Ospite
* 🔄 Creazione automatica delle anagrafiche
* 📊 Integrazione con il modulo Attività
* 📅 Visualizzazione nel Calendario Prenotazioni
* 🔍 Area cliente per il tracciamento dei ticket

<figure><img src="../.gitbook/assets/immagine (975).png" alt=""><figcaption></figcaption></figure>

### Accesso al modulo

Il modulo Richiesta intervento è accessibile tramite un link dedicato che segue la struttura:

{% embed url="https://nomeinstallazione/modules/richiesta/" %}

Dove `nomeinstallazione` rappresenta il nome della tua installazione di OpenSTAManager.

### Modalità di accesso

Al momento dell'accesso al modulo, l'utente può scegliere tra due modalità:

#### 1. Accesso come Utente Registrato

L'utente può effettuare l'accesso utilizzando le proprie credenziali di registrazione. Questa modalità offre vantaggi aggiuntivi:

* Tracciamento storico delle richieste
* Accesso all'area cliente
* Possibilità di visualizzare lo stato dei propri ticket

#### 2. Accesso come Ospite

Gli utenti non registrati possono inviare richieste come ospiti. In questa modalità:

* Non è richiesta la registrazione
* I dati di contatto devono essere forniti nel form
* La richiesta viene comunque elaborata correttamente

<figure><img src="../.gitbook/assets/immagine (1450).png" alt=""><figcaption></figcaption></figure>

### Creazione di una richiesta di intervento

Dopo aver effettuato l'accesso (come utente o ospite), verrà presentata la schermata principale del modulo.

<figure><img src="../.gitbook/assets/immagine (969).png" alt=""><figcaption></figcaption></figure>

#### Procedura

1. **Compilazione del form**: Inserire tutti i dati richiesti nel form di richiesta, inclusi:
   * Informazioni di contatto
   * Descrizione del problema
   * Priorità della richiesta (se applicabile)
   * Altri dettagli rilevanti
2. **Invio della richiesta**: Cliccare sul pulsante **"Richiedi intervento"**
3. **Conferma**: Se la richiesta è andata a buon fine, verrà visualizzato un messaggio di conferma che indica **"Richiesta completata"**

#### Notifiche

Il sistema utilizza un sistema di notifiche (toastr) per fornire feedback immediato all'utente durante l'interazione con il form.

***

### Gestione delle anagrafiche

Una delle funzionalità più utili del modulo è la gestione automatica delle anagrafiche.

#### Creazione automatica

All'apertura di un ticket nel gestionale, il sistema verifica automaticamente se esiste già un'anagrafica con:

* La stessa ragione sociale
* Lo stesso numero di telefono

**Se l'anagrafica non esiste**: Il sistema crea automaticamente una nuova anagrafica corrispondente ai dati forniti nella richiesta.

**Se l'anagrafica esiste**: Il ticket viene associato all'anagrafica esistente.

#### Vantaggi

* ✅ Elimina la duplicazione delle anagrafiche
* ✅ Mantiene il database organizzato
* ✅ Associa automaticamente le richieste ai clienti esistenti

***

### Visualizzazione e gestione dei ticket

#### Nel modulo Richieste di intervento

Il modulo **Richieste di intervento** all'interno del gestionale permette di:

* Visualizzare l'elenco di tutte le richieste ricevute
* Filtrare le richieste per stato, data, cliente
* Accedere ai dettagli di ogni ticket
* Monitorare lo stato di elaborazione

#### Sezionali

Le richieste vengono organizzate in sezionali per facilitare la gestione:

* **Richieste in attesa**: Ticket appena ricevuti e non ancora elaborati
* **Richieste elaborate**: Ticket che sono stati convertiti in interventi

***

### Creazione di interventi dai ticket

Il flusso di lavoro prevede la conversione delle richieste in interventi effettivi.

#### Procedura

1. **Selezionare il ticket**: Cliccare sul ticket desiderato nell'elenco delle richieste
2. **Creare intervento**: Utilizzare l'apposita funzione per creare un intervento direttamente dalla richiesta
3. **Visualizzazione**: L'intervento creato sarà visualizzabile nel modulo **Attività**
4. **Spostamento**: La richiesta viene automaticamente spostata nel sezionale **Richieste elaborate**

#### Vantaggi

* 🔄 Flusso di lavoro continuo
* 📊 Tracciabilità completa
* ⏱️ Risparmio di tempo nell'inserimento dati

***

### Apertura ticket dal Calendario Prenotazioni

Il modulo offre anche la possibilità di creare ticket rapidamente dal Calendario Prenotazioni.

#### Procedura

1. Accedere al modulo **Calendario prenotazioni**
2. Utilizzare il tasto **(+)** per aprire un ticket al volo
3. Compilare i dati essenziali
4. Il ticket verrà visualizzato:
   * Nell'elenco delle richieste
   * Nel calendario

#### Integrazione

Questa funzionalità si integra perfettamente con:

* Il modulo Richieste di intervento
* Il modulo Attività
* Il sistema di calendario

***

### Area Cliente

I clienti possono tenere traccia dei propri ticket aperti accedendo al gestionale e alla propria area cliente.

#### Funzionalità dell'area cliente

* 📋 Visualizzazione dei ticket aperti
* 📊 Monitoraggio dello stato delle richieste
* 📜 Storico delle richieste precedenti
* 📝 Possibilità di aggiungere note o aggiornamenti

#### Accesso

L'accesso all'area cliente richiede:

* Credenziali di registrazione
* Account cliente attivo nel sistema

***

### Sicurezza e Privacy

Il modulo include:

* 🔒 Protezione contro attacchi CSRF
* 🔒 Validazione degli input
* 🔒 Informativa sulla privacy dedicata
* 🔒 Gestione sicura delle credenziali

#### File .htaccess

Il modulo utilizza file `.htaccess` per:

* Proteggere gli accessi non autorizzati
* Configurare le regole di riscrittura
* Limitare l'accesso ai file sensibili

***

### Changelog

#### Versione 5.0 (2026-03-18)

**Aggiunto (Added)**

* File gulpfile.js e package.json per l'automazione delle attività di build
* File rector.php per il refactoring automatico del codice PHP
* Sistema di gestione file JSON per controlli di integrità (modules.php, settings.php, structure.php, tables.php, views.php)
* Configurazione PHP-CS-Fixer per la formattazione automatica del codice

**Modificato (Changed)**

* Allineamento alla versione 2.10
* Ottimizzato stile codice

#### Versione 4.0 (2025-09-29)

**Corretto (Fixed)**

* Migliorie minori file
* Migliorie minori richiesta

#### Versione 3.3 (2025-07-17)

**Corretto (Fixed)**

* Fix modulo richiesta

#### Versione 3.2 (2024-12-19)

**Corretto (Fixed)**

* Fix chiusura errata button

#### Versione 3.1 (2024-11-28)

**Corretto (Fixed)**

* Fix richiesta
* Fix logo
* Fix logo form
* Fix modulo login e loghi

#### Versione 3.0 (2024-11-13)

**Modificato (Changed)**

* Ottimizzato codice per php8.3 e OSM 2.5

**Corretto (Fixed)**

* Fix caricamento modulo richieste di intervento
* Fix installazione modulo
* Fix adattamento bootstrap 3

#### Versione 2.1 (2024-03-20)

**Corretto (Fixed)**

* Fix vari
* Migliorie
* Migliorie minori
* Migliorie modulo
* Gestione login modulo richiesta
* Fix per accesso senza login

#### Versione 2.0 (2023-11-27)

**Modificato (Changed)**

* Allineamento compatibilità calendario con Fullcalendar 6

#### Versione 1.0 (2023-05-11)

**Modificato (Changed)**

* Allineamento 2.4.44

***

**Versione modulo**: 5.0
