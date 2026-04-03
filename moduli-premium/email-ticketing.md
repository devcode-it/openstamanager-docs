---
description: Guida al modulo aggiuntivo Email ticketing in OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/moduli-premium/email-ticketing
---

# 📗 Email ticketing

Il modulo Email Ticketing permette la gestione delle richieste dei clienti via email direttamente dal gestionale OpenSTAManager. Questo modulo converte automaticamente in attività le email ricevute nella casella di posta selezionata. Dall'interno delle attività così create, sarà possibile avviare una vera e propria chat con il cliente mediante il plugin Conversazioni, tenendo traccia così di tutte le interazioni con il cliente.

Il modulo è composto da diversi componenti:

* **Modulo Email Ticketing**: Gestisce la configurazione degli account IMAP e le impostazioni di conversione delle email in attività
* **Plugin Conversazioni**: Permette di visualizzare e gestire le conversazioni con i clienti all'interno delle attività
* **Plugin Anagrafiche Ticketing**: Permette di configurare gli account email dai quali importare le attività per ogni anagrafica
* **Plugin Regole**: Permette di definire regole personalizzate per la gestione delle email in arrivo

{% hint style="info" %}
[Clicca qui](https://shop.openstamanager.com/prodotto/email-ticketing/) per acquistare **Email ticketing**.
{% endhint %}

<figure><img src="../.gitbook/assets/immagine (1218).png" alt=""><figcaption></figcaption></figure>

### Configurazione Account IMAP

#### Creazione Account

La prima cosa da fare è configurare il proprio account IMAP. Per farlo, accedere a **Gestione email > Email ticketing** e cliccare sul tasto (+) per creare un nuovo account email dedicato (oppure configurare l'account predefinito).

<figure><img src="../.gitbook/assets/immagine (274).png" alt=""><figcaption></figcaption></figure>

Il form di configurazione è composto da diverse sezioni:

**1. Dati Casella Email**

In questa sezione devono essere compilati i seguenti campi:

* **Nome account**: Nome identificativo dell'account email
* **Username**: Nome utente per l'accesso alla casella IMAP
* **Password**: Password per l'accesso alla casella IMAP
* **Cartella email processate**: Cartella dell'account email dove verranno archiviate le email processate
* **Hostname**: Indirizzo del server IMAP
* **Porta**: Porta del server IMAP (tipicamente 143 per IMAP non cifrato, 993 per IMAP SSL/TLS)
* **Cifratura connessione**: Tipo di cifratura da utilizzare (Nessuna, TLS, SSL)
* **Disabilita autenticazione**: Opzione per disabilitare l'autenticazione standard (opzionale)
* **Validazione certificato**: Abilita la validazione del certificato SSL/TLS del server

**2. Autenticazione OAuth2**

Il modulo supporta l'autenticazione OAuth2 per i provider Microsoft e Google, che permette un'autenticazione sicura senza memorizzare le credenziali.

Per abilitare l'autenticazione OAuth2:

1. Spuntare l'opzione "Abilita OAuth2"
2. Selezionare il provider (Microsoft o Google)
3. Inserire il Client ID e il Client Secret

<figure><img src="../.gitbook/assets/immagine (276).png" alt=""><figcaption></figcaption></figure>

**Configurazione Google**

1. Accedere su [https://console.developers.google.com/](https://console.developers.google.com/)
2. Creare un progetto apposito OpenSTAManager (esterno) e completare le informazioni per il servizio OAuth (menu "Schermata consenso OAuth" se non automaticamente aperto)
3. Visitare il menu "Credenziali" e creare un nuovo "ID client OAuth 2.0" per Applicazione web con indirizzo di redirect `<baseurl>/plugins/imap/cron/test.php`
4. Copiare `client_id` e `client_secret`

Configurazione:

* Hostname: imap.google.com
* Porta: 993
* Cifratura: SSL
* Class provider: League\OAuth2\Client\Provider\Google

**Configurazione Microsoft**

1. Accedere su [https://portal.azure.com/](https://portal.azure.com/)
2. Navigare su "Azure Active Directory" > "Registrazioni app" ([https://portal.azure.com/#blade/Microsoft\_AAD\_IAM/ActiveDirectoryMenuBlade/RegisteredApps](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RegisteredApps))
3. Aggiungere nuova applicazione OpenSTAManager con indirizzo di redirect `<baseurl>/plugins/imap/cron/test.php`
4. Copiare il `client_id` proposto
5. Per aggiungere un `client_secret`, aggiungere una Application Password tramite "Certificati e segreti" > "Nuovo segreto client" e copiare il codice
6. Nel menu "Autorizzazioni API" aggiungere una nuova autorizzazione sotto "Microsoft Graph" per `IMAP.AccessAsUser.All` e `offline_access`

Configurazione:

* Hostname: outlook.office365.com
* Porta: 993
* Cifratura: SSL
* Class provider: TheNetworg\OAuth2\Client\Provider\Azure

**3. Impostazioni Predefinite**

In questa sezione vengono definite le impostazioni predefinite per le nuove attività create dalle email ricevute:

* **Stato attività**: Imposta lo stato attività di default da settare per le nuove attività importate
* **Tipo attività**: Imposta un tipo di attività di default da settare per le nuove attività importate

<figure><img src="../.gitbook/assets/immagine (277).png" alt=""><figcaption></figcaption></figure>

**4. Flusso Gestione Email**

In questa sezione vengono configurate le notifiche e i template per il flusso di gestione delle email:

**Ricezione Nuova Email**

* **Notifica creazione attività**: Ricevi una notifica quando viene generata una nuova attività
* **Email di notifica**: Indirizzo email per le notifiche di nuove attività
* **Template notifica**: Template per notificare la creazione di un'attività

**Presa in Carico Attività**

* **Notifica al cliente**: Notifica automaticamente al cliente la presa in carico dell'attività
* **Template notifica cliente**: Template per notificare al cliente la presa in carico

**Risposta al Cliente**

* **Template risposta**: Template predefinito per rispondere al cliente

**Risposta dal Cliente**

* **Notifica risposta cliente**: Ricevi una notifica quando il cliente risponde
* **Email notifica risposta**: Indirizzo email per notifiche di risposta dal cliente
* **Template notifica risposta**: Template per notificare le risposte del cliente

<figure><img src="../.gitbook/assets/immagine (280).png" alt=""><figcaption></figcaption></figure>

### Configurazione Anagrafiche

Il modulo email ticketing importa tutte le email presenti in Posta in arrivo. È consigliato quindi creare un'email ad-hoc per questo utilizzo, al fine di evitare l'importazione di attività pregresse già completate o la mancata importazione delle attività per timeout del server.

Dalla schermata di dettaglio di un'anagrafica sarà ora possibile configurare gli account email dai quali importare le attività quando arrivano sotto forma di richieste via mail. Sarà qui possibile selezionare account mail diversi validi al momento della conversione di un'attività, per ogni account mail configurato per l'email ticketing.

#### Collegamento Anagrafiche

Il modulo utilizza diversi metodi per collegare le email ricevute alle anagrafiche:

1. **Plugin Ticketing**: Se l'email ricevuta proviene da un account mail registrato nel plugin "Anagrafiche > Ticketing", l'attività verrà creata collegata a questa anagrafica
2. **Email principale**: Se l'email corrisponde all'email principale di un'anagrafica, l'attività verrà collegata a questa anagrafica
3. **Email sede**: Se l'email corrisponde all'email di una sede dell'anagrafica, l'attività verrà collegata a questa anagrafica e alla sede specificata
4. **Email referente**: Se l'email corrisponde all'email di un referente dell'anagrafica, l'attività verrà collegata a questa anagrafica, alla sede e al referente specificati
5. **Azienda predefinita**: Se la mail ricevuta non è registrata in nessuna anagrafica, l'attività verrà creata collegata all'anagrafica azienda predefinita

<figure><img src="../.gitbook/assets/immagine (281).png" alt=""><figcaption></figcaption></figure>

#### Visualizzazione Conversazioni

Per accedere alle conversazioni di un'attività:

1. Aprire l'attività dal modulo Interventi
2. Cliccare sul plugin "Conversazioni"
3. Verranno visualizzati tutti i messaggi della conversazione, con:
   * Informazioni su mittente, destinatari, oggetto
   * Contenuto dei messaggi
   * Allegati
   * Notifiche di lettura
   * Orari di invio

#### Risposta al Cliente

Per rispondere al cliente:

1. Cliccare sul tasto "Rispondi"
2. Si aprirà il form di risposta con:
   * Selezione dei destinatari (A, CC, CCN)
   * Oggetto precompilato
   * Template di risposta precedentemente selezionato
   * Possibilità di allegare file
   * Opzione "Notifica di lettura" per visualizzare quando il cliente visualizza la mail
3. Compilare il messaggio e cliccare su "Invia"

#### Notifiche di Lettura

Se è stata attivata l'opzione "Notifica di lettura" nell'invio dell'email, sarà possibile visualizzare quando il cliente visualizza la mail. Le notifiche di lettura vengono visualizzate accanto al messaggio inviato.                                                  &#x20;

### Funzionamento dello Script di Importazione

Lo script di importazione (`plugins/imap/cron/index.php`) viene eseguito periodicamente (tramite cron) per importare le email dalla casella IMAP configurata.

#### Processo di Importazione

1. **Connessione IMAP**: Lo script si connette alla casella IMAP configurata utilizzando le credenziali o OAuth2
2. **Lettura Email**: Vengono lette tutte le email presenti nella Posta in arrivo

<figure><img src="../.gitbook/assets/immagine (282).png" alt=""><figcaption></figcaption></figure>

3. **Elaborazione Email**: Per ogni email viene eseguito il seguente processo:
   * Controllo se è una notifica di lettura o un'email normale
   * Se è un'email normale:
     * Controllo se contiene un riferimento a un ticket esistente (tramite `[TICKET #XXX]` nel corpo o nell'oggetto)
     * Se è un ticket esistente, aggiunge il messaggio alla conversazione esistente
     * Se è un nuovo ticket, crea una nuova attività collegata all'anagrafica appropriata
     * Invia notifiche email secondo le configurazioni
     * Salva gli allegati
   * Se è una notifica di lettura, aggiorna lo stato di lettura del messaggio
4. **Archiviazione**: L'email viene spostata nella cartella di archiviazione configurata
5. **Logging**: Tutte le operazioni vengono registrate nel database per il controllo e il debug

<figure><img src="../.gitbook/assets/immagine (283).png" alt=""><figcaption></figcaption></figure>

Cliccando sull'attività e accedendo al plugin Conversazioni sarà ora possibile visualizzare il messaggio ricevuto dal cliente, rispondervi e tener traccia delle conversazioni.

<figure><img src="../.gitbook/assets/immagine (286).png" alt=""><figcaption></figcaption></figure>

Per rispondere al cliente sarà sufficiente cliccare sul tasto Rispondi.

Si aprirà quindi il template di risposta precedentemente selezionato, e spuntando Notifica di lettura, dalle conversazioni sarà possibile visualizzare quando il cliente visualizza la mail.

<figure><img src="../.gitbook/assets/immagine (287).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Vedi anche:
{% endhint %}

{% content-ref url="../configurazioni/configurazione-oauth2.md" %}
[configurazione-oauth2.md](../configurazioni/configurazione-oauth2.md)
{% endcontent-ref %}

#### Gestione Allegati

Gli allegati delle email vengono automaticamente salvati nella cartella `files/conversazioni/` e collegati alla conversazione corrispondente. Gli allegati possono essere visualizzati e scaricati direttamente dall'interfaccia delle conversazioni.

#### Gestione Immagini Inline

Le immagini inline presenti nelle email vengono convertite in formato base64 e visualizzate direttamente nel contenuto del messaggio, senza bisogno di essere scaricate separatamente.

### Testing

Dopo aver configurato la casella IMAP si può testare la corretta configurazione del modulo aprendo sul browser l'indirizzo:

```
https://indirizzo-installazione-osm/plugins/imap/cron/index.php
```

dove `/indirizzo-installazione-osm/` va sostituito con l'indirizzo dell'installazione in uso.

Questo script esegue l'importazione delle email e visualizza l'esito. Da qui è quindi possibile verificare se la configurazione IMAP è corretta, o se il modulo genera errori.

#### Output dello Script

Lo script fornisce un output dettagliato che include:

* Informazioni sulla configurazione dell'account IMAP
* Numero di email trovate
* Dettagli di ogni email elaborata (mittente, oggetto, data)
* Azione eseguita (creazione nuovo ticket, aggiornamento ticket esistente, notifica di lettura)
* Riepilogo finale con:
  * Email elaborate
  * Nuovi ticket creati
  * Ticket esistenti aggiornati
  * Notifiche di lettura
  * Allegati processati
  * Errori riscontrati

#### Configurazione Cron

Una volta terminato il test di importazione occorre inserire in cron l'esecuzione di questo script ogni 5-10 minuti, così che la casella di posta venga scansionata periodicamente per avviare l'importazione automatica delle email.

Esempio di configurazione cron:

```bash
*/5 * * * * php /percorso/della/installazione/plugins/imap/cron/index.php
```

### Variabili Disponibili nei Template

I template di email possono utilizzare le seguenti variabili:

* `{email}`: Email dell'anagrafica
* `{numero}`: Codice dell'intervento
* `{richiesta}`: Richiesta del cliente
* `{descrizione}`: Descrizione dell'intervento
* `{ragione sociale}`: Ragione sociale dell'anagrafica
* `{data}`: Data richiesta dell'intervento
* `{data richiesta}`: Data richiesta dell'intervento
* `{data fine intervento}`: Data fine intervento
* `{id_anagrafica}`: ID dell'anagrafica
* `{stato}`: Stato dell'intervento
* `{prev_email_body}`: Contenuto dell'email precedente
* `{prev_email_data}`: Data dell'email precedente
* `{prev_email_from}`: Mittente dell'email precedente

### Changelog

#### 5.0 (2026-03-17)

**Aggiunto (Added)**

* Gestione file JSON per controlli integrità
* Gestione allegati in invio mail conversazione
* Gestione incolla immagini in fase d'invio mail da conversazione
* Aggiunto codice intervento in invio risposta
* Aggiunto oggetto nella richiesta intervento
* Aggiunto gulpfile e package.json
* Aggiunta php-cs-fixer

**Modificato (Changed)**

* Ottimizzazione script importazione per PEC
* Formattazione stile codice

#### 4.1 (2025-12-16)

**Corretto (Fixed)**

* Ricerca email

#### 4.0 (2025-10-15)

**Aggiunto (Added)**

* Reso compatibile il modulo con la versione 2.5.2 beta
* Aggiunto rector
* Compatibilità con php8.3
* Aggiunto php-cs-fixer

**Corretto (Fixed)**

* Importazione email mittente
* Typo
* Allineamento php8.3
* Miglioramento log (#3)

#### 3.3 (2025-07-15)

**Corretto (Fixed)**

* Match references risposte

#### 3.2 (2025-03-27)

**Corretto (Fixed)**

* Correzione collegamento anagrafica a ticket con riconoscimento della mail

#### 3.1 (2024-10-15)

**Corretto (Fixed)**

* Fix per PHP 8
* Fix per compatibilità OSM 2.5.4

#### 3.0 (2024-06-12)

**Corretto (Fixed)**

* Aggiornamento libreria
* Fix installazione modulo
* Allineamento 2.5.2

#### 2.4 (2024-06-12)

**Corretto (Fixed)**

* Bugfix import e gestione errori import
* Fix minore

#### 2.3 (2024-04-12)

**Aggiunto (Added)**

* Aggiunto collegamento nuova attività a cascata fra anagrafica, referente, sede

**Corretto (Fixed)**

* Modifiche varie
* Fix import
* Fix salvataggio richiesta
* Fix path ckeditor.js
* Fix notifica conversazione

#### 2.2 (2023-11-15)

**Corretto (Fixed)**

* Fix codifica testo email
* Fix per PHP 8.0

#### 2.1 (2023-09-26)

**Aggiunto (Added)**

* Configurazione OAuth2
* Introduzione classe per la lettura
* Supporto per refresh del token
* Base per l'utilizzo di Laminas Mail con IMAP
* Base per OAuth2
* Aggiunta plugin "ticketing" su anagrafiche
* Aggiunta gestione indirizzi email su cui fare il match
* Aggiunta opzione "DISABLE\_AUTHENTICATOR"
* Aggiunte info per regole
* Aggiunta colonna nuovo messaggio
* Gestione invio automatico mail in fase di aggiunta attività
* Numerazione interventi per data richiesta

**Modificato (Changed)**

* Migliorie grafiche in configurazione account IMAP
* Aggiornato campo richiesta in salvataggio
* Aggiornamento creazione intervento con classe
* Aggiornamento di base
* Aggiunti file di supporto
* Adeguamenti per 2.4.11

**Corretto (Fixed)**

* Fix allegati
* Fix get body import email
* Fix scope per Google
* Fix OAuth
* Fix redirect URI
* Gestione allegati .eml senza filename
* Fix invio notifiche
* Fix salvataggio conversazioni
* Fix invio notifiche da test.php
* Fix notifica mail
* Fix salvataggio conversazione
* Bugfix vari
* Fix notifica di lettura
* Fix minori
* Fix scope Google
* Fix salvataggio form
* Fix per lettura con OAuth2 Microsoft
* Fix invio conversazione
* Fix salvataggio allegati
* Fix plugin ticketing
* Fix conversazioni
* Fix varie
* Fix invio mail conversazioni
* Fix invio mail notifica
* Bugfix versione eloquent
* Aggiornamento campo "richiesta" mancante
* Fix refresh token per Microsoft
* Correzioni per accesso con Microsoft
* Correzioni finali per il cambiamento di libreria mail
* Correzione per accesso Microsoft
* Correzioni minori
* Correzione per HTML formattato
* Azzeramento idintervento ad ogni ciclo durante l'importazione
