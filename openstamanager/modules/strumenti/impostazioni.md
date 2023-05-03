---
description: Come modificare le Impostazioni in OpenSTAManager
---

# 🎚 Impostazioni

Il modulo **impostazioni** presenta tutte le impostazioni presenti a gestionale, suddivise per moduli:

<figure><img src="../../../.gitbook/assets/immagine (311).png" alt=""><figcaption></figcaption></figure>

### 🔨 Aggiornamenti

* Attivare o disattivare la notifica di aggiornamenti disponibili di OpenSTAManager.

### 🔨 Anagrafiche

* Impostar il formato codice anagrafica.

Ogni "#" in fase di aggiunta di una nuova anagrafica verrà valorizzato, si può quindi impostare il numero di cifre che verranno mostrate e valorizzate come codice anagrafica.

### 🔨 API

* Lunghezza pagine per API (default)
* Google Maps API key: API key di Google Maps per permettere una corretta visualizzazione delle mappe
* apilayer API key for VAT number: API key verso servizi che permettono di verificare la Partita IVA e inserire automaticamente i dati anagrafici registrati.

### 🔨 Applicazione

* Google Maps API key per Tecnici: API key di Google dove confluiranno le richieste dei tecnici
* Abilitare la visualizzazione dei prezzi nell'APP
* Abilitare la sincronizzare solo dei Clienti per cui il Tecnico ha lavorato in passato
* Impostare il numero di mesi per lo storico delle Attività
* Abilitare la modifica delle attività di altri tecnici, opzione che permette l'inserimento di attività ad altri tecnici
* Abilitare la visualizzazione dei promemoria

### 🔨 Attività

* Abilitare la visualizzazione dei prezzi al tecnico
* Abilitare la stampa per anteprima e firma
* Abilitare l'inserimento di sessioni agli altri tecnici
* Inizio orario lavorativo
* Fine orario lavorativo
* Giorni lavorativi
* Scegliere se notificare al tecnico:
  * l'aggiunta della sessione nell'attività
  * la rimozione della sessione dall'attività
  * l'assegnazione dell'attività
  * la rimozione dell'assegnazione dell'attività
* Stato dell'attività alla chiusura
* Stato dell'attività dopo la firma
* Abilitare la visualizzazione dei promemoria attività ai soli tecnici assegnati
* Abilitare l'espansione automatica della sezione "Dettagli aggiuntivi"
* Abilitare l'invio di alert di occupazione tecnici
* Abilitare la verifica del numero intervento
* Formato ore in stampa
* Descrizione personalizzata in fatturazione
* Stato predefinito dell'attività creata da Dashboard
* Stato predefinito dell'attività alla creazione

### 🔨 Backup

* Numero di backup da mantenere
* Scegliere se abilitare il backup automatico
* Scegliere se permettere il ripristino di backup da file esterni

### 🔨 Contratti

* Condizioni generali di fornitura contratti

### 🔨 Dashboard

* Abilitare i tooltip sul calendario
* Abilitare la visualizzazione della Domenica sul calendario
* Vista dashboard predefinita
* Ora inizio sul calendario
* Ora fine sul calendario
* Abilitare la visualizzazione delle informazioni aggiuntive sul calendario
* Visualizzazione colori sessioni
* Tempo predefinito di snap attività sul calendario

### 🔨 DDT

* Abilitare la modifica automatica dello stato DDT quando fatturati

### 🔨 Fatturazione

* IVA predefinita
* Tipo di pagamento predefinito
* Ritenuta d'acconto predefinita
* Cassa previdenziale predefinita
* Importo marca da bollo
* Soglia minima per l'applicazione della marca da bollo
* Conto aziendale predefinito
* Conto predefinito fatture di vendita
* Conto predefinito fatture di acquisto
* Dicitura fissa fattura
* Metodologia calcolo ritenuta d'acconto predefinito
* Ritenuta previdenziale predefinita
* Abilitare l'addebito della marca da bollo al cliente
* IVA da applicare su marca da bollo
* Descrizione addebito bollo
* Conto predefinito per la marca da bollo
* IVA per lettere d'intento
* Abilitare l'utilizzo di prezzi di vendita comprensivi di IVA
* Liquidazione IVA
* Conto anticipo clienti
* Conto anticipo fornitori
* Descrizione fattura pianificata
* Aggiorna info di acquisto
* Sezionale per autofatture di vendita
* Sezionale per autofatture di acquisto
* Abilitare il blocco ai prezzi inferiori al minimo di vendita
* Abilitare la fatturazione delle attività collegate a contratti, ordini e preventivi
* Abilitare la data di emissione fattura automatica

### 🔨 Fatturazione elettronica

* Abilitare l'allegato di stampa:
  * per fattura verso Privati
  * per fattura verso Aziende
  * per fattura verso PA
* Regime fiscale
* Tipo cassa previdenziale
* Causale ritenuta d'acconto
* ID di autorizzazione indice PA
* OSMCloud Services API Token
* Terzo intermediario
* Abilitare il riferimento dei documenti in Fattura elettronica
* OSMCloud Services API URL
* OSMCloud Services API Version
* Data inizio controlli su stati FE
* Abilitare la movimentazione del magazzino da fatture di acquisto

### 🔨 Generali

* Azienda predefinita
* Nascondere la barra sinistra di default
* Cifre decimali per importi
* CSS Personalizzato
* Abilitare la notifica di presenza utenti sul record
* Timeout notifica di presenza (minuti)
* Prima pagina
* Cifre decimali per quantità
* Tempo di attesa ricerche in secondi
* Logo stampe
* Abilitare esportazione Excel e PDF
* Valuta
* Abilitare il riferimento dei documenti nelle stampe
* Lunghezza in pagine del buffer Datatables
* Autocompletamento form
* Filigrana stampe
* Abilitare scorciatoie da tastiera
* Abilitare modifica viste di Default
* Abilitare canale pre-release per aggiornamenti
* Abilitare totali delle tabelle ristretti alla selezione
* Nascondere la barra dei plugin di default
* Soft quota
* Abilitare la selezione di articoli con quantità minore o uguale a zero in Documenti di Vendita
* Inizio periodo calendario
* Fine periodo calendario
* Abilitare il superamento della soglia quantità dei documenti di origine
* Abilitare l'aggiunta di riferimento tra documenti
* Mantenere riferimenti tra tutti i documenti collegati
* Abilitare l'aggiunta di note delle righe tra documenti
* Dimensione widget predefinita
* Posizione del simbolo valuta

### 🔨 Magazzino

* Abilitare la movimentazione del magazzino durante l'inserimento o eliminazione dei lotti/serial number

### 🔨 Mail

* Numero di giorni di mantenimento della coda di invio

### 🔨 Newsletter

* Numero massimo di tentativi di invio
* Numero email da inviare in contemporanea per account

### 🔨 Ordini

* Abilitare la modifica automatica dello stato ordini fatturati
* Abilitare la conferma automatica delle quantità negli ordini cliente
* Abilitare la conferma automatica delle quantità negli ordini fornitore

### 🔨 Piano dei conti

* Conto per Riepilogo
  * fornitori
  * clienti
* Conto per IVA
  * indetraibile
  * su vendite
  * su acquisti
* Conto per Erario
  * c/ritenute d'acconto
  * c/INPS
  * c/enasarco
* Conto per
  * Apertura conti patrimoniali
  * Chiusura conti patrimoniali
* Conto per autofattura
* Conto di secondo livello per i
  * crediti clienti
  * debiti fornitori

### 🔨 Preventivi

* Condizioni generali di fornitura preventivi
* Abilitare la conferma automatica delle quantità nei preventivi

### 🔨 Scadenzario

* Abilitare l'invio automatico di solleciti
* Template email invio sollecito
* Ritardo in giorni della scadenza della fattura per invio sollecito di pagamento
* Ritardo in giorni dall'ultima email per invio sollecito di pagamento
