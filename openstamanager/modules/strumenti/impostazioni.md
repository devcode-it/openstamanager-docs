---
description: Come modificare le Impostazioni in OpenSTAManager
---

# 🎚 Impostazioni

Il modulo **impostazioni** presenta tutte le impostazioni presenti a gestionale, suddivise per moduli:

<figure><img src="../../../.gitbook/assets/immagine (97).png" alt=""><figcaption></figcaption></figure>

### 🔨 Aggiornamenti

**Attiva aggiornamenti:** Attivare o disattivare la notifica di nuove release del gestionale, questa impostazione non è editabile di default. L'avviso viene visualizzato tra le notifiche:

<figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

### 🔨 Anagrafiche

**Formato codice anagrafica:** Viene qui impostata la maschera applicata alla numerazione delle anagrafiche. Ogni "#" in fase di aggiunta di una nuova anagrafica verrà valorizzato, si può quindi impostare il numero di cifre che verranno mostrate e valorizzate come codice anagrafica.&#x20;

esempio: #### verrà valorizzato con 0001 alla creazione della prima anagrafica.

### 🔨 API

**Lunghezza pagine per API:** definisce il numero di pagine di risposta quando si interroga l'api di OSM.

esempio: la lunghezza pagine impostata è 200 e sono presenti 1000 risultati, verranno visualizzati suddivisi in 5 pagine.

**Google Maps API key:** E' qui possibile inserire l'API key di Google Maps, per poter visualizzare le mappe nei moduli Mappe, Anagrafiche e Attività.

**apilayer API key for VAT number:** API key verso servizi che permettono di verificare la Partita IVA e inserire automaticamente i dati anagrafici registrati.

### 🔨 Applicazione

**Google Maps API key per Tecnici:** API key di Google dove confluiranno le richieste effettuate da utenti appartenenti al gruppo Tecnici, effettuate tramite l'app tecnici.

**Mostra prezzi:** Abilitare la visualizzazione dei prezzi ai tecnici nell'app.

**Sincronizza solo i Clienti per cui il Tecnico ha lavorato in passato:** Abilita la sincronizzazione nell'app delle sole anagrafiche cliente per le quali il tecnico ha delle sessioni nelle attività di cui queste anagrafiche sono impostate come cliente.&#x20;

**Mesi per lo storico attività:** Numero di mesi precedenti alla data odierna di cui conservare le attività sincronizzate nell'app.

**Abilita la modifica di altri tecnici:**&#x20;

**Visualizza promemoria:**

**Visualizza solo promemoria assegnati:**&#x20;

{% hint style="info" %}
Per rendere effettiva la modifica di queste impostazioni è necessario effettuare il reset dell'applicazione ed effettuare nuovamente la sincronizzazione.
{% endhint %}

### 🔨 Attività

**Mostra i prezzi al tecnico:** Disabilitare per non permettere al tecnico di visualizzare i prezzi degli articoli e delle righe all'interno dei documenti.

**Stampa per anteprima e firma:** Selezionare il template di stampa intervento da utilizzare nella sezione anteprima e firma.

**Permetti inserimento sessioni degli altri tecnici:** Permette la modifica delle attività degli altri tecnici, incluso l'inserimento di sessioni di altri utenti del tipo tecnico.

**Inizio orario lavorativo:**

**Fine orario lavorativo:**

**Giorni lavorativi:** Selezionare i giorni di apertura dell'attività, che saranno visualizzati con sfondo bianco in dashboard. I giorni non selezionati verranno invece visualizzati con sfondo rosso e considerati festivi. Il giorno con sfondo giallo invece corrisponde alla data corrente.

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

**Notifica al tecnico l'aggiunta della sessione nell'attività:** Invia automaticamente un'email al tecnico per notificare l'inserimento di nuove sessioni di lavoro che gli sono state assegnate (nell'anagrafica del tecnico deve essere stata specificata un email)

**Notifica al tecnico la rimozione della sessione dall'attività:** Invia automaticamente un'email al tecnico per notificare la rimozione di sessioni di lavoro che erano assegnate a lui e sono successivamente state rimosse (nell'anagrafica del tecnico deve essere stata specificata un email)

**Stato dell'attività alla chiusura:** Stato da impostare all'attività al momento della sua chiusura.

**Stato dell'attività dopo la firma:** Stato da impostare all'attività a seguito della firma del cliente.

**Mostra promemoria attività ai soli Tecnici assegnati:** permette ai tecnici di visualizzare solo le attività senza nessuna sessione, in cui sono stati assegnati come Tecnici assegnato.

**Espandi automaticamente la sezione "Dettagli aggiuntivi":** all'aggiunta di nuove attività viene espansa automaticamente la sezione Dettagli aggiuntivi, permettendo di inserire Data/ora scadenza e l'eventuale Referente.

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

**Alert occupazione tecnici:** Effettua i controlli sulle sessioni inserite per i tecnici, notificando sessioni che presentano conflitti di orario.

**Verifica numero intervento:** Effettua un controllo sulla progressività della numerazione delle attività, mostrando un avviso in caso la numerazione non sia progressiva.

{% hint style="info" %}
Per non visualizzare falsi avvisi è consigliato impostare una maschera nell'apposita sezione in segmenti che includa anche l'anno. Quindi ad esempio ####/yyyy.
{% endhint %}

**Formato ore in stampa:** Selezionare se le ore delle sessioni visualizzate in stampa debbano essere espresse secondo sistema decimale o in sessantesimi.

**Notifica al tecnico l'assegnazione all'attività:** Invia automaticamente un'email al tecnico per notificare l'assegnazione di una nuova attività (nell'anagrafica del tecnico deve essere stata specificata un email)

**Notifica al tecnico la rimozione dell'assegnazione dall'attività:** Invia automaticamente un'email al tecnico per notificare la rimozione dell'assegnazione di un'attività (nell'anagrafica del tecnico deve essere stata specificata un email)

**Descrizione personalizzata in fatturazione:** E' qui possibile definire la descrizione che l'attività assumerà nelle righe di una fattura di vendita una volta aggiunta al documento o procedendo alla fatturazione delle attività da azioni di gruppo.

**Stato predefinito dell'attività da Dashboard:** Definisce lo stato che l'attività assumerà al momento della sua creazione cliccando direttamente in dashboard.

**Stato predefinito dell'attività:** Definisce lo stato che l'attività assumerà al momento della sua creazione dal modulo Attività.

### 🔨 Backup

**Numero di backup da mantenere:** E' qui possibile definire il numero di backup da salvare, verrà eliminato il backup più vecchio alla creazione di ogni nuovo backup.

{% hint style="warning" %}
E' necessario tenere sotto controllo lo spazio disponibile perchè alla creazione di un nuovo backup, nel caso in cui non sia sufficiente, l'operazione verrà interrotta e non verranno effettuati nuovi backup.
{% endhint %}

**Backup automatico:** Se abilitato viene effettuato un backup completo del gestionale secondo le impostazioni definite in zz\_tasks (di default ogni giorno all'1)

**Permetti il ripristino di backup da file esterni:** E' qui possibile disattivare il ripristino di backup da archivi esterni al gestionale.

### 🔨 Contratti

**Condizioni generali di fornitura contratti:** Le condizioni qui inserite verranno riportate in tutti i nuovi contratti creati dal momento della modifica di questa impostazione. Non verranno perciò modificati i contratti precedenti.\


<figure><img src="../../../.gitbook/assets/image (6) (2).png" alt=""><figcaption></figcaption></figure>

### 🔨 Dashboard

**Utilizzare i tooltip sul calendario:**&#x20;

**Visualizzare la domenica sul calendario:** Permette di scegliere se visualizzare o meno la domenica in dashboard.

**Vista dashboard:** Scegliere il tipo di vista predefinita della dashboard tra settimana - mese - giorno - agenda. Questa impostazione verrà applicata a tutti gli utenti.

**Ora inizio sul calendario:** orario di inizio giornata a calendario.

**Ora fine sul calendario:** orario di fine giornata a calendario.

{% hint style="warning" %}
Queste due impostazioni non influenzano gli orari in cui è possibile inserire attività e sessioni, quindi nel caso in cui venga inserita un'attività fuori dagli orari qui indicati, non verrà visualizzata in dashboard.
{% endhint %}

**VIsualizza informazioni aggiuntive sul calendario:** Viene abilitata la sezione _Tutto il giorno_ che permette di visualizzare informazioni aggiuntive sui documenti, come ad esempio l'accettazione e conclusione dei preventivi.

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

**Visualizzazione colori sessioni:** E' possibile scegliere come visualizzare le sessioni in dashboard, decidendo se visualizzare lo sfondo e il bordo dell'attività del colore assegnato al tecnico o allo stato dell'attività.

**Tempo predefinito di snap attività sul calendario:**

### 🔨 DDT

**Cambia automaticamente stato ddt fatturati**: se questa impostazione è abilitata, blocca la possibilità di modificare manualmente lo stato dei ddt. Al momento della fatturazione di un ddt gli cambia automaticamente lo stato in fatturato.

### 🔨 Fatturazione

**Iva predefinita:**

**Tipo di pagamento predefinito:**

**Ritenuta d'acconto predefinita:**

**Cassa previdenziale predefinita:**

**Importo marca da bollo:**

**Soglia minima per l'applicazione della marca da bollo:**

**Conto aziendale predefinito:**

**Conto predefinito fatture di vendita:**

**Conto predefinito fatture di acquisto:**

**Dicitura fissa fattura:**

**Metodologia calcolo ritenuta d'acconto predefinito:**

**Ritenuta previdenziale predefinita:**

**Addebita marca da bollo al cliente:**

**Iva da applicare su marca da bollo:**

**Descrizione addebito bollo:**

**Conto predefinito per la marca da bollo:**

**Iva per lettere d'intenti:**

**Utilizza prezzi di vendita comprensivi di IVA:**

**Liquidazione iva:**

**Conto anticipi clienti:**

**Conto anticipo fornitori:**

**Descrizione fattura pianificata:**

**Aggiorna info di acquisto:**

**Sezionale per autofatture di vendita:**

**Sezionale per autofatture di acquisto:**

**Bloccare i prezzi inferiori al minimo di vendita:**

**Permetti fatturazione delle attività collegate a contratti:**

**Data emissione fattura automatica:**

**Permetti fatturazione delle attività collegate a ordini:**

**Permetti fatturazione delle attività collegate a preventivi:**

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
