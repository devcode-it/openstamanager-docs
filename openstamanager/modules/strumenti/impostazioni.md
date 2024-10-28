---
description: Come modificare le Impostazioni in OpenSTAManager
---

# 🎚️ Impostazioni

Il modulo **impostazioni** presenta tutte le impostazioni presenti a gestionale, suddivise per moduli:

<figure><img src="../../../.gitbook/assets/immagine (651).png" alt=""><figcaption></figcaption></figure>

### 🔨 Aggiornamenti

**Attiva aggiornamenti:** Attivare o disattivare la notifica di nuove release del gestionale, questa impostazione non è editabile di default. L'avviso viene visualizzato tra le notifiche:

<figure><img src="../../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

**Abilita canale pre-release per aggiornamenti:** Consente di visualizzare l'uscita di nuove release Beta del gestionale.

### 🔨 Anagrafiche

**Formato codice anagrafica:** Viene qui impostata la maschera applicata alla numerazione delle anagrafiche. Ogni "#" in fase di aggiunta di una nuova anagrafica verrà valorizzato, si può quindi impostare il numero di cifre che verranno mostrate e valorizzate come codice anagrafica.&#x20;

esempio: #### verrà valorizzato con 0001 alla creazione della prima anagrafica.

### 🔨 API

**Lunghezza pagine per API:** Definisce il numero di pagine di risposta quando si interroga l'api di OSM.

esempio: la lunghezza pagine impostata è 200 e sono presenti 1000 risultati, verranno visualizzati suddivisi in 5 pagine.

**apilayer API key for VAT number:** API key per il servizio di validazione della Partita IVA.

### 🔨 Applicazione

**Google Maps API key per Tecnici:** API key di Google dove confluiranno le richieste effettuate da utenti appartenenti al gruppo Tecnici, effettuate tramite l'app tecnici.

**Mostra prezzi\*:** Abilitare la visualizzazione dei prezzi ai tecnici nell'app.

**Sincronizza solo i Clienti per cui il Tecnico ha lavorato in passato\*:** Abilita la sincronizzazione nell'app delle sole anagrafiche cliente per le quali il tecnico ha delle sessioni nelle attività di cui queste anagrafiche sono impostate come cliente.&#x20;

**Mesi per lo storico attività\*:** Numero di mesi precedenti alla data odierna di cui conservare le attività sincronizzate nell'app.

**Stato dell'attività alla chiusura\*:** Stato in cui impostare l'attività al momento della sua chiusura.

**Abilita la modifica di altri tecnici\*:** Permette la modifica delle attività degli altri tecnici da app, incluso l'inserimento di sessioni di altri utenti del tipo tecnico.

**Visualizza promemoria\*:** Se disabilitato non permette la sincronizzazione dei promemoria in app.

**Visualizza solo promemoria assegnati\*:**  Permette ai tecnici di visualizzare solo le attività senza nessuna sessione, in cui sono stati assegnati come Tecnici assegnato.

**Permetti l'accesso agli amministratori\*:** Se questa impostazione è abilitata, l'accesso all'app è consentita agli amministratori.

**Limita la visualizzazione degli impianti a quelli gestiti dal tecnico\*:** Verranno sincronizzati in app unicamente gli impianti in cui il tecnico è assegnato.

{% hint style="info" %}
\*Per rendere effettiva la modifica di queste impostazioni è necessario effettuare il reset dell'applicazione ed effettuare nuovamente la sincronizzazione
{% endhint %}

{% content-ref url="../../app-tecnici/v3.0.30.md" %}
[v3.0.30.md](../../app-tecnici/v3.0.30.md)
{% endcontent-ref %}

### 🔨 Attività

**Mostra i prezzi al tecnico:** Disabilitare per non permettere al tecnico di visualizzare i prezzi degli articoli e delle righe all'interno dei documenti.

**Stampa per anteprima e firma:** Selezionare il template di stampa intervento da utilizzare nella sezione anteprima e firma.

**Permetti inserimento sessioni degli altri tecnici:** Permette la modifica delle attività degli altri tecnici da gestionale, incluso l'inserimento di sessioni di altri utenti del tipo tecnico.

**Giorni lavorativi:** Selezionare i giorni di apertura dell'attività, che saranno visualizzati con sfondo bianco in dashboard. I giorni non selezionati verranno invece visualizzati con sfondo rosso e considerati festivi. Il giorno con sfondo giallo invece corrisponde alla data corrente.

<figure><img src="../../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

**Notifica al tecnico l'aggiunta della sessione nell'attività:** Invia automaticamente un'email al tecnico per notificare l'inserimento di nuove sessioni di lavoro che gli sono state assegnate (nell'anagrafica del tecnico deve essere stata specificata un email).

**Notifica al tecnico la rimozione della sessione dall'attività:** Invia automaticamente un'email al tecnico per notificare la rimozione di sessioni di lavoro che erano assegnate a lui e sono successivamente state rimosse (nell'anagrafica del tecnico deve essere stata specificata un email).

**Stato dell'attività dopo la firma:** Stato da impostare all'attività a seguito della firma del cliente.

**Espandi automaticamente la sezione "Dettagli aggiuntivi":** All'aggiunta di nuove attività viene espansa automaticamente la sezione Dettagli aggiuntivi, permettendo di inserire Data/ora scadenza e l'eventuale Referente.

<figure><img src="../../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

**Alert occupazione tecnici:** Effettua i controlli sulle sessioni inserite per i tecnici, notificando sessioni che presentano conflitti di orario.

**Verifica numero intervento:** Effettua un controllo sulla progressività della numerazione delle attività, mostrando un avviso in caso la numerazione non sia progressiva.

{% hint style="info" %}
Per non visualizzare falsi avvisi è consigliato impostare una maschera nell'apposita sezione in segmenti che includa anche l'anno. Quindi ad esempio ####/yyyy.
{% endhint %}

**Formato ore in stampa:** Selezionare se le ore delle sessioni visualizzate in stampa debbano essere espresse secondo sistema decimale o in sessantesimi.

**Notifica al tecnico l'assegnazione all'attività:** Invia automaticamente un'email al tecnico per notificare l'assegnazione di una nuova attività (nell'anagrafica del tecnico deve essere stata specificata un email).

**Notifica al tecnico la rimozione dell'assegnazione dall'attività:** Invia automaticamente un'email al tecnico per notificare la rimozione dell'assegnazione di un'attività (nell'anagrafica del tecnico deve essere stata specificata un email).

**Descrizione personalizzata in fatturazione:** E' qui possibile definire la descrizione che l'attività assumerà nelle righe di una fattura di vendita una volta aggiunta al documento o procedendo alla fatturazione delle attività da azioni di gruppo.

**Stato predefinito dell'attività da Dashboard:** Definisce lo stato che l'attività assumerà al momento della sua creazione cliccando direttamente in dashboard.

**Stato predefinito dell'attività:** Definisce lo stato che l'attività assumerà al momento della sua creazione dal modulo Attività.

**Numero di minuti di avanzamento delle sessioni delle attività:** Specifica di quanti minuti aumentare e diminuire le sessioni di lavoro in modifica sessione nelle attività.

### 🔨 Backup

**Numero di backup da mantenere:** E' qui possibile definire il numero di backup da salvare, verrà eliminato il backup più vecchio alla creazione di ogni nuovo backup.

{% hint style="warning" %}
E' necessario tenere sotto controllo lo spazio disponibile perchè alla creazione di un nuovo backup, nel caso in cui non sia sufficiente, l'operazione verrà interrotta e non verranno effettuati nuovi backup.
{% endhint %}

**Backup automatico:** Se abilitato viene effettuato un backup completo del gestionale secondo le impostazioni definite in zz\_tasks (di default ogni giorno all'1).

**Permetti il ripristino di backup da file esterni:** E' qui possibile disattivare il ripristino di backup da archivi esterni al gestionale.

### 🔨 Contratti

**Condizioni generali di fornitura contratti:** Le condizioni qui inserite verranno riportate in tutti i nuovi contratti creati dal momento della modifica di questa impostazione. Non verranno perciò modificati i contratti precedenti.\


<figure><img src="../../../.gitbook/assets/image (595).png" alt=""><figcaption></figcaption></figure>

**Crea contratto rinnovabile di default:** Se abilitata, alla creazione di un nuovo contratto, esso sarà impostato come rinnovabile.

**Giorni di preavviso di default:** Se abilitata, definisce il numero di giorni di preavviso rinnovo che verranno impostati alla creazione di una nuova attività

### 🔨 Dashboard

**Utilizzare i tooltip sul calendario:**  Abilita la visualizzazione di tooltip sul calendario.

**Visualizzare la domenica sul calendario:** Permette di scegliere se visualizzare o meno la domenica in dashboard.

**Vista dashboard:** Scegliere il tipo di vista predefinita della dashboard tra settimana - mese - giorno - agenda. Questa impostazione verrà applicata a tutti gli utenti.

**Ora inizio sul calendario:** Orario di inizio giornata a calendario.

**Ora fine sul calendario:** Orario di fine giornata a calendario.

{% hint style="warning" %}
Queste due impostazioni non influenzano gli orari in cui è possibile inserire attività e sessioni, quindi nel caso in cui venga inserita un'attività fuori dagli orari qui indicati, non verrà visualizzata in dashboard.
{% endhint %}

**Visualizza informazioni aggiuntive sul calendario:** Viene abilitata la sezione _Tutto il giorno_ che permette di visualizzare informazioni aggiuntive sui documenti, come ad esempio l'accettazione e conclusione dei preventivi.

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

**Visualizzazione colori sessioni:** E' possibile scegliere come visualizzare le sessioni in dashboard, decidendo se visualizzare lo sfondo e il bordo dell'attività del colore assegnato al tecnico o allo stato dell'attività.

**Tempo predefinito di snap attività sul calendario:** Intervallo di tempo utilizzato per lo spostamento di un'attività in dashboard, non può superare il tempo totale dell'intervallo impostato di default a 15 minuti.

### 🔨 DDT

**Cambia automaticamente stato ddt fatturati**: Se questa impostazione è abilitata, blocca la possibilità di modificare manualmente lo stato dei ddt. Al momento della fatturazione di un ddt gli cambia automaticamente lo stato in fatturato.

### 🔨 Fatturazione

**Iva predefinita:** E' qui possibile definire l'aliquota iva predefinita che verrà utilizzata nell'inserimento righe nei documenti se nella scheda anagrafica o articolo non ne è definita una diversa.

**Tipo di pagamento predefinito:** Viene qui definita la modalità di pagamento predefinita, che verrà selezionata nei documenti dove non è presente un'anagrafica con associata una modalità di pagamento predefinito.

**Ritenuta d'acconto predefinita:** E' qui possibile selezionare la ritenuta d'acconto da utilizzare nei documenti di default, verrà così inserita in tutti i nuovi documenti in uscita.

**Cassa previdenziale predefinita:** E' qui possibile definire la cassa previdenziale da utilizzare nei documenti di default, verrà così inserita in tutti i nuovi documenti in uscita.

**Importo marca da bollo:** Va qui specificato l'importo della marca da bollo.

**Soglia minima per l'applicazione della marca da bollo:** Va  quispecificato l'importo superato il quale va aggiunta la marca da bollo nei documenti.

**Conto aziendale predefinito:** Va qui definito il conto predefinito da utilizzare nei pagamenti, nel caso non ne sia specificato uno diverso associato al tipo di pagamento selezionato.

**Conto predefinito fatture di vendita:** Conto utilizzato di default per movimentare le fatture di vendita.

**Conto predefinito fatture di acquisto:** Conto utilizzato di default per movimentare le fatture di acquisto.

**Dicitura fissa fattura:** Viene qui definita la dicitura fissa che verrà mostrata a piè di pagina della fattura di vendita.

**Metodologia calcolo ritenuta d'acconto predefinito:** Viene qui deciso se calcolare la ritenuta d'acconto sull'imponibile o sull'imponibile + IVA di default.

**Ritenuta previdenziale predefinita:** Viene qui definita la ritenuta previdenziale predefinita.

**Descrizione addebito bollo:** Nome del bollo da applicare al documento.

**Conto predefinito per la marca da bollo:** Conto predefinito selezionato per risolvere la marca da bollo in fase di registrazione in prima nota del pagamento del documento.

**Iva per lettere d'intenti:** Iva utilizzata di default per i documenti collegati a lettere d'intento.

**Utilizza prezzi di vendita comprensivi di IVA:** Si può da qui abilitare la gestione degli importi ivati per i prezzi di vendita.

**Liquidazione iva:** Viene qui impostato se la liquidazione iva viene effettuata mensilmente o trimestralmente.&#x20;

{% hint style="info" %}
Questa impostazione influirà sul calcolo della maggiorazione 1% in fase di stampa liquidazione IVA.
{% endhint %}

**Conto anticipi clienti:** Conto utilizzato di default per la gestione di anticipi da clienti.

**Conto anticipo fornitori:** Conto utilizzato di default per la gestione di anticipi a fornitori.

**Descrizione fattura pianificata:** E' qui possibile definire la dicitura delle rate di fatturazione utilizzata nel plugin fatturazione pianificata in contratti.

**Aggiorna info di acquisto:** Viene selezionata l'impostazione di default che verrà preselezionata in fase di importazione fattura elettronica

**Sezionale per autofatture di vendita:** Sezionale impostato di default per la registrazione delle autofattura tra i documenti in uscita.

**Sezionale per autofatture di acquisto:** Sezionale impostato di default per la registrazione delle autofattura tra i documenti in entrata.

**Bloccare i prezzi inferiori al minimo di vendita:** Non permette di inserire nei documenti prezzi di vendita inferiori al prezzo minimo impostato.

**Permetti fatturazione delle attività collegate a contratti:** Permette di fatturare le attività anche se sono collegate a un contratto.

**Data emissione fattura automatica:** Se questa opzione è abilitata non viene permessa l'emissione di fatture con data precedente a quella dell'ultimo documento emesso, la data viene pertanto modificata e corretta automaticamente con la data odierna.

**Permetti fatturazione delle attività collegate a ordini:** Permette di fatturare le attività anche se sono collegate a un ordine.

**Permetti fatturazione delle attività collegate a preventivi:** Permette di fatturare le attività anche se sono collegate a un preventivo.

**Data inizio verifica contatore fattura di vendita:** Definisce la data a partire dalla quale verificare la progressività di numerazione delle fatture di vendita.

**Raggruppa attività per tipologia in fattura:** Raggruppa le attività in base alla loro tipologia in fattura di vendita.

### 🔨 Fatturazione elettronica

**Allega stampa per fattura verso Privati:** Se abilitato, allega una copia di cortesia della fattura all'XML della fattura di vendita, per clienti di tipologia Privato.

**Allega stampa per fattura verso Aziende:** Se abilitato, allega una copia di cortesia della fattura all'XML della fattura di vendita, per clienti di tipologia Azienda.

**Allega stampa per fattura verso PA:** Se abilitato, allega una copia di cortesia della fattura all'XML della fattura di vendita, per clienti di tipologia Ente Pubblico.

**Regime Fiscale:** Definisce il regime fiscale dell'azienda.

**Tipo Cassa Previdenziale:**  Definisce il tipo della rivalsa.

**Causale ritenuta d'acconto:** Permette di scegliere la causale della ritenuta d'acconto tra quelle presenti nell'elenco.

<figure><img src="../../../.gitbook/assets/image (337).png" alt=""><figcaption></figcaption></figure>

**Authorization ID Indice PA:** Token necessario per la verifica dei codici fiscali delle pubbliche amministrazioni, ottenibile da: [https://www.indicepa.gov.it/ipa-portale/dati-statistiche/web-service/richiedi-authorization-id](https://www.indicepa.gov.it/ipa-portale/dati-statistiche/web-service/richiedi-authorization-id)

**OSMCloud Services API Token:** Se si è sottoscritto al servizio di invio/ricezione fatture elettroniche con OSM, viene qui riportato il token univoco per inviare e scaricare fatture da CompEd.

**Terzo intermediario:** Può essere specificato un intermediario incaricato dell'invio delle fatture elettroniche.

**Riferimento dei documenti in Fattura Elettronica:** Se abilitato nelle righe vengono riportati i riferimenti ai documenti da cui sono state importate le righe, specificando quindi se provengono da ordini, preventivi o contratti.

**OSMCloud Services API URL:** Indirizzo per contattare services, necessario per l'invio e ricezione di fatture elettroniche.

**OSMCloud Services API Version:** Versione delle API di services, necessario per l'invio e ricezione di fatture elettroniche.

**Data inizio controlli su stati FE:** Specificare qui la data dalla quale iniziare a fare controlli sulle fatture di vendita, per segnalare eventuali ritardi nell'invio o fatture che presentano ricevute di scarto.

**Movimenta magazzino da fatture di acquisto:** E' possibile scegliere se movimentare il magazzino con l'inserimento/importazione di fatture di acquisto.

**Rimuovi avviso fatture estere:** Abilitare per rimuovere gli avvisi relativi a ritardo nell'invio di fatture elettroniche di vendita verso anagrafiche estere. Da attivare nel caso non vengano inviate le fatture elettroniche estere.

**Creazione seriali in import FE:** Determina il valore predefinito dell'impostazione Creazione seriali in fase di importazione delle fatture di acquisto.

**Giorni validità fattura scartata:** Numero di giorni a disposizione per poter correggere una fattura scartata dallo SDI prima di non poter più utilizzare il suo numero di fatturazione. Una volta superati i giorni indicati, è necessario emettere una nuova fattura e questa passa in stato Non valida.

### 🔨 Generali

**Azienda predefinita:** Viene qui selezionata l'anagrafica azienda.

**Nascondere la barra sinistra di default:** Se abilitata, il menu di sinistra verrà nascosto in automatico all'accesso ai moduli, mostrando solo le icone.

<figure><img src="../../../.gitbook/assets/image (293).png" alt=""><figcaption></figcaption></figure>

**Cifre decimali per importi:** Numero di cifre decimali da visualizzare per numeri corrispondenti a importi.&#x20;

{% hint style="info" %}
Tutti i valori totali hanno un numero di decimali fissato a 2.
{% endhint %}

**CSS Personalizzato:** E' qui possibile inserire del CSS personalizzato per modificare la grafica del gestionale e nascondere determinati campi.

**Attiva notifica di presenza utenti sul record:** Viene mostrato un avviso nel caso in cui un altro utente sia all'interno dello stesso documento, per evitare salvataggi che vadano a sovrascrivere gli stessi dati.

<figure><img src="../../../.gitbook/assets/image (328).png" alt=""><figcaption></figcaption></figure>

**Timeout notifica di presenza (minuti):** Mostrare il numero di minuti dopo i quali non mostrare più l'avviso di presenza di altri utenti all'interno dello stesso documento.

**Prima pagina:** Selezionare la pagina che verrà visualizzata in seguito al login.

**Cifre decimali per quantità:** Numero di cifre decimali da visualizzare per numeri corrispondenti a quantità.&#x20;

**Tempo di attesa ricerche in secondi:** Limite di tempo superato il quale, in fase di digitazione caratteri in un filtro di una tabella, viene avviata la ricerca.

**Logo stampe:** Percorso del file impostato come logo nelle stampe, definibile in fase di configurazione dell'installazione o tramite scheda anagrafica azienda.

{% content-ref url="../../../guide/esempi/impostare-logo-nelle-stampe.md" %}
[impostare-logo-nelle-stampe.md](../../../guide/esempi/impostare-logo-nelle-stampe.md)
{% endcontent-ref %}

**Abilita esportazione Excel e PDF:** Permette l'esportazione della tabella selezionata in PDF e Excel

<figure><img src="../../../.gitbook/assets/image (331).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Questa impostazione non influenza nessuna funzionalità delle azioni di gruppo.
{% endhint %}

**Valuta:** La valuta da utilizzare nel gestionale.

**Visualizza riferimento su ogni riga in stampa:** Se disabilitato, raggruppa il riferimento ai documenti collegati in un'unica riga, se abilitato riporta i riferimenti ai documenti in ogni riga.

**Lunghezza in pagine del buffer Datatables:** E' qui possibile stabilire il numero di risultati da esportare in fase di esportazione e stampa, a numeri più elevati corrispondono maggiori tempi di risposta per il caricamento di un numero di record maggiori.

{% content-ref url="../../../guide/esempi/esportare-e-stampare-tabelle-con-molti-record.md" %}
[esportare-e-stampare-tabelle-con-molti-record.md](../../../guide/esempi/esportare-e-stampare-tabelle-con-molti-record.md)
{% endcontent-ref %}

**Autocompletamento form:** Se abilitato permette l'autoinserimento di valori al momento dell'inserimento da tastiera

**Filigrana stampe:** Percorso del file impostato come filigrana nelle stampe, definibile in fase di configurazione dell'installazione o tramite scheda anagrafica azienda.

**Attiva scorciatoie da tastiera:** E' possibile abilitare o disabilitare le scorciatoie da tastiera visualizzate nell'help.

**Modifica Viste di default:** Se abilitato permette la modifica delle viste di default nel modulo Viste.

**Totali delle tabelle ristretti alla selezione:** Nei vari moduli, i totali a fondo pagina delle tabelle assumono il valore dei record selezionati, in caso ci sia almeno una riga selezionata.

<figure><img src="../../../.gitbook/assets/image (447).png" alt=""><figcaption></figcaption></figure>

**Nascondere la barra dei plugin di default:** Se abilitato, la barra dei plugin rimane chiusa fino alla sua apertura.

**Soft quota:** Valore espresso in Giga superato il quale viene visualizzato un avviso di spazio in esaurimento.

**Permetti selezione articoli con quantità minore o uguale a zero in Documenti di Vendita:** Se abilitata, permette di inserire come righe delle fatture di vendita e ddt in uscita degli articoli non disponibili a magazzino, quindi con quantità negativa.

**Inizio periodo calendario:** Viene qui definita la data di inizio che viene impostata di default nel filtro temporale del gestionale, se lasciato vuoto imposta automaticamente il 01/01 dell'anno corrente.

**Fine periodo calendario:** Viene qui definita la data di fine che viene impostata di default nel filtro temporale del gestionale, se lasciato vuoto imposta automaticamente il 31/12 dell'anno corrente.

<figure><img src="../../../.gitbook/assets/image (335).png" alt=""><figcaption></figcaption></figure>

**Permetti il superamento della soglia quantità dei documenti di origine:** Permette di modificare il valore della quantità degli articoli presenti in fattura, superando il valore impostato nelle righe del documento collegato.

**Aggiungi riferimento tra documenti:** Permette l'aggiunta del riferimento al documento nella descrizione della riga importata.

**Mantieni riferimenti tra tutti i documenti collegati:** Permette l'aggiunta di riferimenti tra le righe, di tutti i documenti collegati.

**Aggiungi le note delle righe tra documenti:** Permette di riportare le note della riga in fase di importazione tra documenti.

**Dimensione widget predefinita:** Permette di impostare la classe del widget, definendone le dimensioni. Tuttavia è possibile forzare la dimensione dei vari widget da Strumenti/Stato dei servizi, per impostare dimensioni personalizzate per ogni singolo widget.

{% hint style="info" %}
Ricordando che bootstrap prevede un numero di celle totali pari a 12 per riga, volendo ad esempio impostare il numero di widget per riga pari a 6, sarà sufficiente impostare come dimensione predefinita "col-md-2".
{% endhint %}

**Posizione del simbolo valuta:** E' Possibile scegliere se visualizzare il simbolo valuta prima o dopo il numero.

**Tile server OpenStreetMap:** Imposta il tile server per la visualizzazione di OpenStreetMap, per modificare la visualizzazione delle mappe.

**Sistema di firma:** E' qui possibile scegliere se firmare le attività tramite il metodo di firma classico o tramite tavoletta Wacom.

**Tipo di sconto predefinito:** Definisce il tipo di sconto predefinito tra unitario e percentuale.

**Cifre decimali per importi in stampa:** Definisci il numero di decimali che presenteranno gli importi nelle stampe.

**Cifre decimali per quantità in stampa:** Definisci il numero di decimali che presenteranno le quantità nelle stampe.

**Cifre decimali per totali in stampa:** Definisci il numero di decimali che presenteranno i totali nelle stampe.

**Listino cliente predefinito:** In fase di creazione di una nuova anagrafica cliente, definisce il listino cliente da associarvi di default.

**Lingua:** Definisce la lingua in cui impostare il gestionale.

**Ridimensiona automaticamente le immagini caricate:** Se abilitato, gli allegati caricati verranno ridimensionati per ottimizzare lo spazio.

**Larghezza per ridimensionamento immagini:** Definisce la larghezza delle immagini che verranno ridimensionate.

### 🔨 Magazzino

**Movimenta il magazzino durante l'inserimento o eliminazione dei lotti/serial number:** Se abilitato, all'inserimento di seriali in una scheda articolo, viene aggiunto il corrispondente numero di articoli alla giacenza.

**Serial number abilitato di default:** Se abilitato ogni nuovo articolo creato in Magazzino e da importazione di fattura di acquisto avrà il serial number abilitato.

**Magazzino cespiti:** Magazzino cespiti per la stampa dei cespiti nel modulo Articoli,  è possibile scegliere tra le sedi collegate all'azienda.

### 🔨 Mail

**Numero di giorni di mantenimento della coda di invio:** Vengono specificati il numero di giorni dopo i quali eliminare un'email dalla coda di invio.

### 🔨 Newsletter

**Numero massimo di tentativi:** Numero di tentativi da effettuare per l'invio di una mail.&#x20;

**Numero email da inviare in contemporanea per account:** Numero di email presenti in coda di invio da inviare contemporaneamente per ogni account.

### 🔨 Ordini

**Cambia automaticamente stato ordini fatturati:** Se questa impostazione è abilitata, blocca la possibilità di modificare manualmente lo stato degli ordini. Al momento della fatturazione di un ordine gli cambia automaticamente lo stato in fatturato.

**Conferma automaticamente le quantità negli ordini cliente:** Le quantità degli articoli presenti nelle righe degli ordini cliente vengono confermate automaticamente.

**Conferma automaticamente le quantità negli ordini fornitore:** Le quantità degli articoli presenti nelle righe degli ordini fornitore vengono confermate automaticamente.

**Visualizza numero ordine cliente:** Se abilitata, utilizza nei documenti il numero d'ordine del cliente al posto del numero interno dell'ordine.

### 🔨 Piano dei conti

**Conto per Riepilogativo fornitori:** Di default 000010 - Riepilogativo fornitori

**Conto per Riepilogativo clienti:** Di default 000010 - Riepilogativo clienti

**Conto per Iva indetraibile:** Di default 000030 - Iva indetraibile

**Conto per Iva su vendite:** Di default 000010 - Iva su vendite

**Conto per Iva su acquisti:** Di default 000020 - Iva su acquisti

**Conto per Erario c/ritenute d'acconto:** Di default 000060 - Erario c/ritenute d'acconto

**Conto per Erario c/INPS:** Di default 000010 - Erario c/INPS

**Conto per Erario c/enasarco:** Di default 000070 - Erario c/enasarco

**Conto per Apertura conti patrimoniali:** Di default 000010 - Apertura conti patrimoniali

**Conto per Chiusura conti patrimoniali:** Di default 000010 - Chiusura conti patrimoniali

**Conto per autofattura:** Di default 000010 - Compensazione per autofattura

**Conto di secondo livello per i crediti clienti:** Di default 110 - Crediti clienti e crediti diversi

**Conto di secondo livello per i debiti fornitori:** Di default 110 - Debiti fornitori e debiti diversi

### 🔨 Preventivi

**Condizioni generali di fornitura preventivi:** Le condizioni qui inserite verranno riportate in tutti i nuovi preventivi creati dal momento della modifica di questa impostazione. Non verranno perciò modificati i preventivi precedenti.

**Conferma automaticamente le quantità nei preventivi:**  Le quantità degli articoli presenti nelle righe dei preventivi vengono confermate automaticamente.

**Esclusioni default preventivi:** E' qui possibile definire il testo inserito di default tra le esclusioni dei preventivi.

### 🔨 Scadenzario

**Invio solleciti in automatico:** Invia automaticamente delle email di sollecito secondo le tempistiche definite nelle impostazioni

**Template email primo sollecito:** Template email utilizzato per il primo sollecito di pagamento di una rata scaduta.

**Ritardo in giorni della scadenza della fattura per invio sollecito pagamento:** Numero di giorni dopo i quali verrà inviato il primo sollecito di pagamento, utilizzando il template selezionato nell'impostazione precedente.

**Ritardo in giorni dall'ultima email per invio sollecito pagamento:** Numero di giorni a partire dalla data di invio del sollecito precedente, allo scadere dei quali verranno inviati il secondo e terzo sollecito e la notifica di mancato pagamento.

**Template email secondo sollecito:** Template email utilizzato per il secondo sollecito di pagamento di una rata scaduta.

**Template email terzo sollecito:** Template email utilizzato per il terzo sollecito di pagamento di una rata scaduta.

**Template email mancato pagamento dopo i solleciti:** Template email utilizzato per la notifica di mancato pagamento a seguito dell'invio di 3 solleciti, all'indirizzo selezionato nell'impostazione successiva.

**Indirizzo email mancato pagamento dopo i solleciti:** Indirizzo email sul quale verrà notificato il mancato pagamento a seguito dell'invio di 3 solleciti al cliente, allo scadere dei giorni previsti per la notifica scadenza se l'incasso del pagamento non viene registrato.

**Template email promemoria scadenza:** Template email utilizzato per la notifica dell'imminente scadenza con giorni di anticipo definiti nell'impostazione successiva.

**Intervallo di giorni in anticipo per invio promemoria scadenza:** Specifica il numero di giorni alla scadenza in cui inviare un promemoria di pagamento notificando la scadenza imminente

### 🔨 Tavoletta Wacom

**Licenza Wacom SDK - Key:** Chiave di licenza per l'utilizzo della tavoletta grafica Wacom.

**Sfondo firma tavoletta Wacom:** Colore di sfondo impostato per la firma nella tavoletta grafica Wacom.

**Luminosità firma Wacom:** Luminosità impostata di default per la tavoletta grafica Wacom.

**Contrasto firma Wacom:** Contrasto impostato di default per la tavoletta grafica Wacom.

**Secondi timeout tavoletta Wacom:** E' qui possibile impostare i secondi di default prima dello spegnimento automatico della tavoletta Wacom.

**Licenza Wacom SDK - Secret:** E' qui possibile impostare il secret generato con la generazione della licenza.

{% content-ref url="../../../guide/esempi/generazione-di-una-chiave-di-licenza-wacom.md" %}
[generazione-di-una-chiave-di-licenza-wacom.md](../../../guide/esempi/generazione-di-una-chiave-di-licenza-wacom.md)
{% endcontent-ref %}
