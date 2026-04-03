---
description: Configurazione Tavoletta Wacom per firma sul gestionale
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/WzoKFijlVGKTMgti0acZ/configurazioni/tavoletta-wacom
---

# 📙 Tavoletta Wacom

Questa guida spiega come configurare e utilizzare una tavoletta grafica Wacom per la firma digitale in OpenSTAManager.

### Requisiti

#### Browser Supportati

Per utilizzare correttamente la tavoletta Wacom per la firma digitale, è necessario utilizzare un browser che supporti l'API WebHID.

**Browser Compatibili**

✅ **Browser basati su Chromium** (raccomandati):

* **Google Chrome** versione 89 o superiore
* **Microsoft Edge** versione 89 o superiore
* **Opera** versione 75 o superiore
* **Brave** (versione recente)
* **Vivaldi** (versione recente)

**Browser Non Compatibili**

❌ **Browser che NON supportano l'API WebHID**:

* **Mozilla Firefox**: Non supporta l'API WebHID nativamente
* **Safari**: Non supporta l'API WebHID
* **Internet Explorer**: Non supportato

⚠️ **Nota importante**: La tavoletta Wacom richiede il supporto per l'API `navigator.hid` del browser. Solo i browser basati su Chromium supportano questa API nativamente. Si consiglia vivamente di utilizzare Google Chrome o Microsoft Edge per la migliore compatibilità.

#### Requisiti di Connessione

* **HTTPS obbligatorio**: La funzionalità di firma con tavoletta Wacom richiede che OpenSTAManager sia accessibile tramite connessione HTTPS sicura. Non funzionerà con HTTP.
* **Connessione internet attiva**: La firma Wacom richiede comunicazione con i server Wacom

### Configurazione

#### Passo 1: Ottenere le Chiavi API

Per attivare la funzionalità di firma con tavoletta Wacom, è necessario disporre delle chiavi API fornite da Wacom:

1. [Generare una chiave valida](../guide/esempi/generazione-di-una-chiave-di-licenza-wacom.md)
2. Riceverai due chiavi:
   * **Licenza Wacom SDK - Key**
   * **Licenza Wacom SDK - Secret**

⚠️ **Nota**: Le chiavi API sono strettamente legate al dominio su cui è installato OpenSTAManager. Per utilizzare la funzionalità in ambiente di sviluppo o locale, potrebbe essere necessario richiedere chiavi di test a Wacom.

#### Passo 2: Inserire le Chiavi in OpenSTAManager

1. Accedi a OpenSTAManager con un account amministratore
2. Naviga in **Strumenti → Impostazioni**
3. Cerca e configura le seguenti impostazioni:

**Impostazioni Obbligatorie**

* **Sistema di firma**: Imposta su `Tavoletta Wacom` (opzioni disponibili: "Base", "Tavoletta Wacom")
* **Licenza Wacom SDK - Key**: Inserisci la chiave ricevuta da Wacom
* **Licenza Wacom SDK - Secret**: Inserisci il segreto ricevuto da Wacom

**Impostazioni Opzionali (per personalizzazione)**

* **Secondi timeout tavoletta Wacom**: Definisce il numero di secondi prima del timeout della tavoletta (valore consigliato: 30-60 secondi)
* **Sfondo firma tavoletta Wacom**: Colore di sfondo per la firma (es. "#ffffff" per bianco)
* **Luminosità firma Wacom**: Regola la luminosità della firma (valore numerico, es. 0)
* **Contrasto firma Wacom**: Regola il contrasto della firma (valore numerico, es. 0)
* **Stampa per anteprima e firma**: Seleziona il template di stampa da utilizzare per l'anteprima della firma

4. Salva le modifiche

### Utilizzo della Tavoletta

La tavoletta Wacom viene utilizzata per firmare gli **interventi** in OpenSTAManager.

#### Come firmare un intervento

1. Apri un intervento che richiede la firma
2. Clicca sul pulsante **Anteprima e firma** (o **Firma** a seconda della configurazione)
3. Verrà visualizzata l'anteprima del documento con il pulsante **Firma**
4. Clicca su **Firma**
5. Se la tavoletta è configurata correttamente, verrà aperta l'interfaccia di firma Wacom
6. Firma utilizzando la penna sulla tavoletta
7. Conferma la firma cliccando su "Conferma"
8. La firma verrà salvata automaticamente

#### Note sull'Utilizzo

* Il sistema utilizza automaticamente il metodo "Base" se viene rilevato un dispositivo mobile, indipendentemente dall'impostazione configurata
* Se il browser non supporta `navigator.hid`, verrà visualizzato un messaggio di errore
* È possibile cancellare e rifirmare se necessario prima di salvare definitivamente

### Risoluzione dei Problemi

#### Errore: "Questa funzione richiede una connessione HTTPS"

**Causa**: OpenSTAManager non è accessibile tramite HTTPS

**Soluzione**:

* Configura un certificato SSL/TLS sul server
* Assicurati di accedere a OpenSTAManager tramite `https://` e non `http://`

#### Errore: "navigator.hid non è supportato da questo browser!"

**Causa**: Il browser in uso non supporta l'API WebHID necessaria per la tavoletta Wacom

**Soluzione**:

* Installa o utilizza **Google Chrome** (versione 89 o superiore)
* Installa o utilizza **Microsoft Edge** (versione 89 o superiore)
* Altri browser compatibili: Opera (v75+), Brave, Vivaldi
* ❌ **NON utilizzare**: Firefox, Safari o Internet Explorer (non supportano WebHID)
* Verifica che le estensioni del browser non blocchino le API HID

#### La tavoletta non viene rilevata

**Possibili cause e soluzioni**:

* Verifica che la tavoletta sia collegata correttamente al computer
* Assicurati di aver installato i driver Wacom più recenti
* Prova a riavviare il browser
* Verifica di utilizzare un browser compatibile (Chrome, Edge, Opera, Brave, Vivaldi)
* ❌ Assicurati di NON utilizzare Firefox o Safari (non supportano WebHID)
* Controlla che nessun'altra applicazione stia utilizzando la tavoletta

#### Errore durante la firma

**Possibili cause e soluzioni**:

* Controlla che le chiavi API siano state inserite correttamente
* Verifica che l'impostazione "Sistema di firma" sia impostata su "Tavoletta Wacom"
* Controlla la console del browser per eventuali errori JavaScript
* Assicurati di avere una connessione internet attiva
* Verifica che il dominio corrisponda a quello per cui sono state rilasciate le chiavi API

#### Il modulo di firma non appare

**Possibili cause e soluzioni**:

* Verifica che l'impostazione "Sistema di firma" sia configurata correttamente
* Controlla che non ci siano estensioni del browser che bloccano gli script
* Prova in modalità incognito o disabilitando temporaneamente le estensioni
* Verifica che l'intervento non sia già completato o firmato

#### Firma di bassa qualità o poco leggibile

**Soluzione**:

* Regola l'impostazione "Luminosità firma Wacom"
* Regola l'impostazione "Contrasto firma Wacom"
* Modifica il colore di sfondo tramite "Sfondo firma tavoletta Wacom"
* Verifica che la penna della tavoletta sia pulita e funzionante



***
