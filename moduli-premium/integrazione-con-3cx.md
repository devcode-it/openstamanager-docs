---
description: >-
  Guida al modulo aggiuntivo di integrazione del Centralino 3CX in
  OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/moduli-premium/integrazione-con-3cx
---

# 📗 Integrazione con 3CX

Il modulo Centralino 3CX è dedicato alla gestione delle operazioni di integrazione del gestionale OpenSTAManager con il sistema di centralini 3CX, al fine di registrare le chiamate e fornire una consultazione rapida delle informazioni disponibili.

Sono disponibili due moduli distinti:

* **Centralino 3CX** gestisce la registrazione delle chiamate e la visualizzazione dello storico;

<figure><img src="../.gitbook/assets/immagine (1235).png" alt=""><figcaption></figcaption></figure>

* **Operatori 3CX** permette l'assegnazione di anagrafiche Tecnico a uno specifico interno di chiamata, con gestione del relativo storico delle assegnazioni.

<figure><img src="../.gitbook/assets/immagine (1234).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
[Clicca qui ](https://shop.openstamanager.com/prodotto/3cx/)per procedere all'acquisto
{% endhint %}

Il centralino 3CX si registra automaticamente nel browser in utilizzo una volta effettuato l'accesso a OpenSTAManager. Tutti gli utenti ricevono una notifica desktop all'arrivo di ogni chiamata in entrata, con 10-15 secondi di anticipo prima che il telefono inizi a suonare effettivamente.

Chrome mostra in automatico un popup per abilitare le notifiche, mentre per Firefox le notifiche sono disabilitate di default e compare un pulsante in alto a sinistra dell'interfaccia. Il click sulla notifica apre la schermata di riepilogo della chiamata, dove è possibile aggiungere una descrizione e modificare lo stato tra Aperta e Gestita.

**Attenzione**: la chiamata va posta come Gestita solo a seguito della chiusura fisica della telefonata.

Una volta aperti i dettagli della chiamata, è possibile procedere alla creazione o all'associazione con una Attività.

{% hint style="warning" %}
**Attenzione**: le chiamate in uscita non generano mai una notifica, ma sono accessibili dall'elenco principale del modulo Centralino 3CX.
{% endhint %}

<figure><img src="../.gitbook/assets/immagine (1236).png" alt=""><figcaption></figcaption></figure>

### Caratteristiche principali

#### Integrazione API

Il sistema espone le seguenti API REST per l'integrazione con 3CX:

* **contact-lookup**: Ricerca automatica di contatti in base al numero telefonico
* **contact-creation**: Creazione automatica di nuovi contatti (opzionale)
* **call-journaling**: Registrazione completa delle chiamate (in entrata, in uscita, perse, senza risposta)
* **call-notification**: Invio notifiche desktop in tempo reale per chiamate in entrata

#### Normalizzazione numeri telefonici

Il sistema implementa una normalizzazione avanzata dei numeri telefonici che:

* Rimuove caratteri di formattazione (spazi, punti, trattini, parentesi, segni più)
* Gestisce correttamente i prefissi internazionali (0039, +39)
* Supporta ricerche parziali per numeri corti (< 6 cifre)
* Cerca automaticamente tra anagrafiche, sedi e referenti

#### Gestione notifiche desktop

* Utilizzo di Service Worker e Web Push API
* Supporto per Chrome e Firefox
* Notifiche con azioni rapide (Info, Anagrafica)
* Gestione automatica delle credenziali push nella tabella `3cx_push`

#### Widget di statistica

* **Statistiche Numeri**: Analisi numeri conosciuti vs sconosciuti con dettagli su chiamate e durata
* **Statistiche Telefonate**: Statistiche per operatore con numero chiamate risposte e tempo totale

#### Configurazione 3CX

La configurazione di 3CX deve essere effettuata attraverso il menu **Impostazioni -> CRM**, aggiungendo una personalizzazione in _Seleziona una soluzione CRM_.

Caricare il file [`OpenSTAManager.xml`](https://openstamanager.xml:1) e configurare i seguenti parametri:

**Configurazione generale**

* **API Key**: Token di accesso all'API del gestionale (preferibilmente di Amministratore)
* **URL di OpenSTAManager**: URL di base per raggiungere il gestionale

**Opzionali**

* **Enable Contact Creation**: Abilita la creazione automatica di nuovi contatti (default: False)
* **New Contact First Name**: Nome per nuovi contatti (default: \[Number])
* **New Contact Last Name**: Cognome per nuovi contatti (default: Nuovo contatto (3CX))
* **Enable Call Journaling**: Abilita la registrazione delle chiamate (default: True)
* **Call Subject**: Oggetto delle chiamate (default: 3CX PhoneSystem Call)
* **Answered Inbound Call**: Testo per chiamate in entrata risposte
* **Missed Call**: Testo per chiamate perse
* **Answered Outbound Call**: Testo per chiamate in uscita risposte
* **Unanswered Outbound Call**: Testo per chiamate in uscita senza risposta

Il campo _Interrogazione CRM_ deve essere impostato a "Sempre".

#### Configurazione notifiche desktop

Per abilitare le notifiche desktop, è necessario:

1. Includere il file JavaScript `centralino/ajax/caller.js` in tutte le pagine del gestionale modificando il file `config.inc.php`:

```php
// Ulteriori file CSS e JS da includere
$assets = [
    'css' => [],
    'print' => [],
    'js' => [
        'https://miainstallazione.osmbusiness.it/modules/3cx_centralino/ajax/caller.js',
    ],
];
```

2. Aggiungere i file delle chiavi VAPID nel percorso `modules/3cx_centralino/keys/`:
   * `public_key.txt`: Chiave pubblica per le notifiche
   * `private_key.txt`: Chiave privata per le notifiche

#### Configurazione operatori

Il modulo Operatori 3CX permette di assegnare anagrafiche di tipo Tecnico a specifici interni di chiamata:

1. Accedere al modulo Operatori 3CX
2. Aggiungere un nuovo operatore specificando:
   * **Interno**: Il numero interno telefonico
   * **Anagrafica**: Il tecnico associato all'interno
3. Il sistema mantiene automaticamente lo storico delle assegnazioni (soft delete)

### Funzionamento

#### Flusso delle chiamate

1. **Lookup contatto** (contact-lookup):
   * 3CX invia una richiesta di ricerca contatto per ogni chiamata
   * Il sistema normalizza il numero e cerca tra anagrafiche, sedi e referenti
   * Viene creata una chiamata con durata 0 e stato "Aperta"
   * Per chiamate in entrata, viene inviata una notifica push
2. **Notifica chiamata** (call-notification):
   * Il sistema invia notifiche desktop a tutti i browser registrati
   * Le notifiche includono azioni rapide per accedere ai dettagli
   * Click sulla notifica apre la schermata di riepilogo della chiamata
3. **Journaling chiamata** (call-journaling):
   * Al termine della chiamata, 3CX invia i dettagli completi
   * Il sistema aggiorna la chiamata esistente o ne crea una nuova
   * Se la chiamata è stata associata a un intervento, viene creata una sessione di tipo "CALL"

#### Gestione delle chiamate

**Chiamate in entrata**

* Ricevono notifica desktop 10-15 secondi prima che il telefono inizi a suonare
* Chrome mostra automaticamente un popup per abilitare le notifiche
* Firefox richiede l'abilitazione manuale tramite pulsante in alto a sinistra
* Click sulla notifica apre la schermata di riepilogo

**Chiamate in uscita**

* Non generano notifiche desktop
* Sono accessibili dall'elenco principale del modulo Centralino 3CX
* Vengono registrate automaticamente al termine della chiamata

**Stati della chiamata**

* **Aperta**: Chiamata in corso o appena ricevuta
* **Gestita**: Chiamata completata (da impostare solo dopo la chiusura fisica della telefonata)

#### Associazione con interventi

Dai dettagli della chiamata è possibile:

* Creare una nuova Attività collegata
* Associare la chiamata a un intervento esistente
* Aggiungere descrizioni e note

Se la chiamata viene associata a un intervento, il sistema crea automaticamente una sessione di tipo "CALL" con i tempi della chiamata.

### Test delle chiamate

Per testare il funzionamento del sistema, è possibile simulare chiamate tramite curl:

#### Chiamata in entrata senza risposta

```bash
curl -X POST -d '{"token":"il_tuo_token","version":"3cx","resource":"call-journaling","Number":"numero_chiamante","CallDirection":"Inbound", "CallStartTimeLocal":"2025-07-25 10:00:00", "CallEndTimeLocal":"2025-07-25 10:00:00", "Answered":0, "DurationSeconds":0, "Duration":"00:00:00", "CallType":"Voice", "Description":"Chiamata di test"}' 'https://miainstallazione.osmbusiness.it/api/'
```

#### Chiamata in entrata con risposta

```bash
curl -X POST -d '{"token":"il_tuo_token","version":"3cx","resource":"call-journaling","Number":"numero_chiamante","CallDirection":"Inbound", "CallStartTimeLocal":"2025-07-25 10:00:00", "CallEndTimeLocal":"2025-07-25 10:05:00", "Answered":1, "DurationSeconds":300, "Duration":"00:05:00", "CallType":"Voice", "Description":"Chiamata di test"}' 'https://miainstallazione.osmbusiness.it/api/'
```

***

## Changelog

### 5.0 (2026-03-10)

#### Aggiunto

* Generazione file JSON per verifica integrità moduli
* Aggiunta gulpfile e package.json per build automatizzata
* Ricerca con Google del numero su una nuova tab quando questo non è stato riconosciuto

#### Correzioni

* Ricerca associazione numero che inizia con 39 per coincidenza, non perché ha il prefisso internazionale
* `filtraNumero()` non rimuove più 39 in modo indiscriminato

### 4.1 (2025-09-30)

#### Aggiunto

* Introduzione widget Statistiche Numeri
* Introduzione widget Statistiche Telefonate
* Aggiunto periodo dinamico al widget Statistiche Telefonate
* Implementata normalizzazione avanzata numeri telefonici

#### Modificato

* Refactor: statistiche per operatore

#### Correzioni

* Inclusione corretta delle date nel periodo
* Escluse anagrafiche cancellate dalla ricerca numeri telefonici
* Aggiunto controllo validità numero prima della ricerca (no vuoto, minimo 3 cifre)
* Matching numeri telefonici

### 4.0 (2025-07-25)

#### Modificato

* Miglioria modulo centralino

### 3.1 (2024-11-22)

#### Correzioni

* Rimozione dipendenza carbon
* Orario fine chiamata
* Salvataggio orario inizio chiamata

### 3.0 (2024-06-14)

#### Aggiunto

* Aggiunto php-cs-fixer
* Aggiunto rector
* Allineato a OSM 2.5.2

### 2.0 (2023-10-06)

#### Aggiunto

* Gestione input telefono

### 1.0 (2023-04-27)

#### Aggiunto

* Rilascio iniziale del modulo centralino 3CX
