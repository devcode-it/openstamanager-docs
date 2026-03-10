---
description: Guida al modulo aggiuntivo Gestione SMS in OpenSTAManager
metaLinks:
  alternates:
    - https://app.gitbook.com/s/I8PynmXUVfCOtwZFC1I6/moduli-premium/gestione-sms
---

# 📗 Gestione SMS

{% hint style="info" %}
**Gestione SMS** è un modulo acquistabile da **OpenstaSTAManager** che permette l'invio di SMS dall'interno dei moduli, definiti da specifici template e tenendo traccia dello storico degli sms inviat&#x69;**.**
{% endhint %}

#### Caratteristiche Principali

* ✅ **Invio SMS dai moduli**: Integrazione nativa con i moduli di OpenSTAManager
* ✅ **Template personalizzati**: Creazione di template con variabili dinamiche
* ✅ **Gestione account**: Supporto per provider SMS multipli
* ✅ **Coda di invio**: Sistema automatico di gestione degli SMS in coda
* ✅ **Storico completo**: Tracciamento di tutti gli SMS inviati, in uscita e non inviati
* ✅ **Supporto WhatsApp**: Invio di messaggi WhatsApp tramite lo stesso provider
* ✅ **Gestione errori**: Sistema automatico di retry con tentativi multipli



#### Provider SMS Supportati

Attualmente il modulo supporta i seguenti provider:

| Provider         | API           | Note                                         |
| ---------------- | ------------- | -------------------------------------------- |
| **Smshosting**   | REST API v0.1 | Provider principale, supporta SMS e WhatsApp |
| _Altri provider_ | _In sviluppo_ | Estensibile tramite architettura plugin      |

### Installazione

#### Installazione tramite OpenSTAManager

1. Accedi al tuo account OpenSTAManager
2. Naviga nella sezione **Marketplace**
3. Cerca il modulo **"Gestione SMS"**
4. Acquista e installa il modulo
5. Segui le istruzioni di configurazione automatica

### Panoramica dei Moduli

Dopo l'installazione, verranno aggiunte le seguenti voci al menu di OpenSTAManager:

```
Gestione SMS
├── Template SMS
├── Coda SMS
├── Account SMS
└── Gestione SMS
```

#### Struttura dei Moduli

**1. Template SMS**

Permette di creare e gestire i template per l'invio di SMS. I template possono contenere variabili dinamiche che vengono sostituite automaticamente con i dati del record selezionato.



<figure><img src="../.gitbook/assets/immagine (453).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/immagine (948).png" alt=""><figcaption></figcaption></figure>

**2. Coda SMS**

Visualizza lo stato di tutti gli SMS:

* SMS inviati con successo
* SMS in attesa di invio
* SMS non inviati (con gestione errori)
* Storico completo con filtri temporali

<figure><img src="../.gitbook/assets/immagine (762).png" alt=""><figcaption></figcaption></figure>

**3. Account SMS**

Gestisce la configurazione degli account con i provider SMS. È possibile configurare più account per diversi provider o per diverse finalità.

<figure><img src="../.gitbook/assets/immagine (954).png" alt=""><figcaption></figcaption></figure>

**4. Gestione SMS**

Modulo principale che fornisce una panoramica delle statistiche e delle configurazioni del sistema.

***

### Configurazione Account SMS

#### Creazione di un Nuovo Account

Per configurare un nuovo account SMS:

1. Accedi al modulo **Account SMS** dal menu
2. Clicca su **Aggiungi**
3. Compila i campi richiesti:
   * **Nome account**: Un nome descrittivo per identificare l'account
   * **Provider**: Seleziona il provider (es. Smshosting)
   * **Auth key**: Chiave di autenticazione fornita dal provider
   * **Auth secret**: Segreto di autenticazione fornito dal provider
   * **Timeout**: Tempo di attesa tra gli invii (in millisecondi, default: 100)

#### Configurazione Smshosting

Per configurare un account con Smshosting:

1. Accedi al tuo account su [www.smshosting.it](https://www.smshosting.it)
2. Naviga nella sezione **Sviluppatori**



<figure><img src="../.gitbook/assets/immagine (611).png" alt=""><figcaption></figcaption></figure>

3. Clicca su **API REST, HTTP e SOAP**

<figure><img src="../.gitbook/assets/immagine (758).png" alt=""><figcaption></figcaption></figure>

4. Copia i dati di autenticazione dal riquadro azzurro:
   * **Auth key**: Chiave API
   * **Auth secret**: Segreto API

<figure><img src="../.gitbook/assets/immagine (956).png" alt=""><figcaption></figcaption></figure>

5. Inserisci i dati nel modulo di configurazione

#### Opzioni Avanzate

* **Timeout**: Configura il tempo di attesa tra l'invio di SMS consecutivi dallo stesso account. Questo è utile per evitare limitazioni del provider.
* **Multi-account**: È possibile configurare più account per distribuire il carico o utilizzare provider diversi.

***

### Gestione Template SMS

#### Creazione di un Template

1. Accedi al modulo **Template SMS**
2. Clicca su **Aggiungi**
3. Compila i campi:
   * **Nome**: Nome descrittivo del template
   * **Account**: Seleziona l'account SMS da utilizzare
   * **Modulo**: Seleziona il modulo di OpenSTAManager (es. Anagrafiche, Preventivi, ecc.)
   * **Corpo**: Inserisci il testo dell'SMS con le variabili

#### Variabili nei Template

Le variabili disponibili dipendono dal modulo selezionato. Le variabili vengono inserite nel formato `{nome_variabile}`.

**Esempio di Template per Anagrafiche**

```
Gentile {ragione_sociale},
La sua fattura n. {numero_fattura} del {data_fattura}
è disponibile per un importo di {importo}€.
Grazie per la fiducia!
```

**Variabili Comuni**

| Variabile           | Descrizione          | Modulo             |
| ------------------- | -------------------- | ------------------ |
| `{ragione_sociale}` | Nome dell'anagrafica | Anagrafiche        |
| `{nome}`            | Nome del contatto    | Anagrafiche        |
| `{cognome}`         | Cognome del contatto | Anagrafiche        |
| `{telefono}`        | Numero di telefono   | Anagrafiche        |
| `{numero}`          | Numero documento     | Preventivi/Fatture |
| `{data}`            | Data documento       | Preventivi/Fatture |
| `{importo}`         | Importo totale       | Preventivi/Fatture |

#### Best Practices per i Template

* Mantieni i messaggi concisi (massimo 160 caratteri per SMS standard)
* Utilizza variabili chiare e descrittive
* Verifica sempre il template prima di utilizzarlo
* Crea template specifici per ogni scenario comunicativo

***

### Invio SMS

#### Invio dai Moduli

Dopo aver creato un template per un modulo specifico, puoi inviare SMS direttamente da quel modulo:

1. Apri il modulo desiderato (es. Anagrafiche, Preventivi, ecc.)
2. Seleziona il record di interesse
3. Cerca l'opzione **Invia SMS** o il pulsante dedicato
4. Seleziona il template da utilizzare
5. Verifica il numero di telefono (autocompilato dall'anagrafica)
6. Conferma l'invio

<figure><img src="../.gitbook/assets/immagine (963).png" alt=""><figcaption></figcaption></figure>

Il numero di telefono a cui inviare l'SMS verrà autocompilato con il numero presente nell'anagrafica cliente selezionata.

<figure><img src="../.gitbook/assets/immagine (438).png" alt=""><figcaption></figcaption></figure>

#### Flusso di Invio

1. **Creazione**: L'SMS viene creato e inserito nella coda
2. **Elaborazione**: Il sistema elabora automaticamente la coda
3. **Invio**: L'SMS viene inviato tramite il provider configurato
4. **Conferma**: Lo stato viene aggiornato (inviato/non inviato)
5. **Retry**: In caso di errore, il sistema riprova automaticamente (massimo 10 tentativi)

#### Invio WhatsApp

Il modulo supporta anche l'invio di messaggi WhatsApp tramite lo stesso provider Smshosting. Il processo è identico all'invio SMS, ma il messaggio viene recapitato tramite WhatsApp.

#### Gestione del Numero di Telefono

Il numero di telefono viene automaticamente compilato con:

* Il numero presente nell'anagrafica cliente selezionata
* Il numero presente nel record del modulo corrente
* Il prefisso internazionale viene gestito automaticamente

***

### Coda SMS

#### Visualizzazione della Coda

Il modulo **Coda SMS** mostra tutti gli SMS con i seguenti stati:

| Stato               | Descrizione              | Icona |
| ------------------- | ------------------------ | ----- |
| **Inviato**         | SMS inviato con successo | ✅     |
| **In elaborazione** | SMS in attesa di invio   | ⏳     |
| **Non inviato**     | SMS con errori di invio  | ❌     |

#### Filtri e Ricerca

La coda SMS supporta i seguenti filtri:

* **Periodo temporale**: Filtra per data di creazione o invio
* **Account**: Filtra per account SMS utilizzato
* **Template**: Filtra per template utilizzato
* **Utente**: Filtra per utente che ha creato l'SMS
* **Stato**: Filtra per stato dell'SMS

#### Azioni sulla Coda

* **Visualizza dettagli**: Mostra il contenuto dell'SMS e le informazioni di invio
* **Riprova invio**: Forza il reinvio di SMS non inviati
* **Elimina**: Rimuove l'SMS dalla coda
* **Esporta**: Esporta la lista degli SMS in formato CSV/Excel

#### Sistema Automatico di Retry

Il sistema implementa un meccanismo automatico di retry:

* **Massimo 10 tentativi** per ogni SMS
* **Intervallo di 4 ore** tra i tentativi
* **Gestione timeout** tra invii consecutivi dallo stesso account
* **Logging dettagliato** delle risposte del provider

#### Monitoraggio in Tempo Reale

Il sistema fornisce notifiche in tempo reale sullo stato dell'invio:

* **Icona nella barra superiore**: Mostra lo stato dell'elaborazione
* **Contatore progressivo**: Visualizza il numero di SMS inviati rispetto al totale
* **Messaggi di stato**: "Invio sms in corso..." o "Invio sms completato!"

***

