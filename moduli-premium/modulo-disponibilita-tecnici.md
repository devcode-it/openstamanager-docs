---
description: Guida al modulo aggiuntivo Disponibilità tecnici in OpenSTAManager
---

# 📗 Disponibilità tecnici

**Disponibilità tecnici** è un modulo aggiuntivo per OpenSTAManager che rappresenta una rivisitazione avanzata del modulo Dashboard. Questo modulo è stato progettato specificamente per organizzare l'attività dei singoli tecnici con maggiore efficienza e controllo.

Il modulo permette di visualizzare e gestire le attività dei tecnici in un calendario interattivo, offrendo una visione chiara e immediata della disponibilità dei tecnici in base a diversi intervalli temporali: mese, settimana o giorno.

<figure><img src="../.gitbook/assets/immagine (15).png" alt=""><figcaption></figcaption></figure>

#### Vantaggi principali

* **Visualizzazione intuitiva**: Le attività segnate a calendario vengono suddivise per operatore
* **Gestioni efficienti**: Un rapido colpo d'occhio permette di conoscere la disponibilità dei tecnici
* **Pianificazione semplice**: Creazione rapida di nuove attività direttamente dal calendario
* **Integrazione completa**: Si integra perfettamente con il sistema di gestione interventi di OpenSTAManager

***

### Caratteristiche Principali

1. **Calendario Interattivo**
   * Visualizzazione mensile, settimanale e giornaliera
   * Supporto per drag & drop degli interventi
   * Visualizzazione a timeline per tecnico
   * Indicatore di data/ora corrente
2. **Gestione Attività**
   * Creazione rapida di nuove attività
   * Modifica diretta degli interventi nel calendario
   * Visualizzazione dettagliata con tooltip
   * Gestione dei promemoria da pianificare
3. **Filtro Tecnici**
   * Selezione multipla di tecnici da visualizzare
   * Possibilità di nascondere tecnici specifici
4. **Personalizzazione Visuale**
   * Colori personalizzabili per tecnici e stati
   * Opzioni di visualizzazione degli eventi
   * Configurazione dei giorni lavorativi
   * Gestione dei tooltip informativi
5. **Integrazione Anagrafiche**
   * Plugin dedicato per la gestione tecnici
   * Controllo della visibilità dei tecnici
   * Sincronizzazione automatica con le anagrafiche

***

### Installazione

#### Acquisto del Modulo

Il modulo "Disponibilità tecnici" è disponibile per l'acquisto dal marketplace ufficiale di OpenSTAManager.

1. Accedi al marketplace di OpenSTAManager
2. Cerca "Disponibilità tecnici"
3. Procedi all'acquisto seguendo le istruzioni

#### Installazione tramite OpenSTAManager

1. **Ricezione link di download del modulo compatibile**
2. **Caricamento nel Sistema**
   * Accedi al pannello amministrativo di OpenSTAManager
   * Naviga in `Strumenti` > `Aggiornamenti`
   * Carica lo ZIP nella sezione Installa Aggiornamenti
   * Clicca su Scarica aggiornamento
   * Segui le istruzioni a schermo
3. **Verifica dell'Installazione**
   * Il modulo dovrebbe apparire nel menu principale

***

### Configurazione Iniziale

#### Prima Configurazione

Dopo l'installazione, è necessario configurare alcune impostazioni base:

1. **Accesso al Modulo**
   * Clicca su "Disponibilità tecnici" nel menu principale
   * Verrà visualizzata la schermata principale del calendario
2. **Configurazione dei Tecnici**
   * I tecnici vengono caricati automaticamente dalle anagrafiche
   * Solo i tecnici con l'opzione "show\_disponibilita" attiva verranno visualizzati
3. **Impostazioni del Calendario**
   * Configura l'orario di lavoro (inizio e fine)
   * Seleziona i giorni lavorativi
   * Personalizza i colori per stati e tecnici

#### Impostazioni di Base

Le impostazioni principali possono essere configurate in `Strumenti` > `Impostazioni` > `Dashboard`:

* **Ora inizio sul calendario**: Orario di inizio della visualizzazione giornaliera
* **Ora fine sul calendario**: Orario di fine della visualizzazione giornaliera
* **Giorni lavorativi**: Giorni della settimana considerati lavorativi
* **Visualizzare la domenica sul calendario**: Mostra/nasconde la domenica
* **Utilizzare i tooltip sul calendario**: Abilita i tooltip informativi
* **Visualizza informazioni aggiuntive sul calendario**: Mostra dettagli aggiuntivi

***

### Interfaccia Utente

#### Layout Principale

L'interfaccia del modulo è divisa in tre sezioni principali:

**1. Filtro Tecnici**

Posizionato nella parte superiore, permette di:

* Selezionare i tecnici da visualizzare nel calendario
* Utilizzare una selezione multipla
* Mantenere la selezione tra le sessioni
* Aggiungere nuovi tecnici direttamente dal filtro

<figure><img src="../.gitbook/assets/immagine (16).png" alt=""><figcaption></figcaption></figure>

**2. Calendario Disponibilità Tecnici**

La sezione centrale mostra il calendario interattivo con:

* Viste multiple (mese, settimana, giorno)
* Timeline divisa per tecnico
* Eventi colorati in base allo stato e al tecnico
* Indicatore della data/ora corrente

<figure><img src="../.gitbook/assets/immagine (17).png" alt=""><figcaption></figcaption></figure>

**3. Promemoria da Pianificare**

Se presenti, questa sezione mostra:

* Interventi non ancora pianificati
* Promemoria da contratti
* Selettore per mese
* Eventi trascinabili nel calendario

<figure><img src="../.gitbook/assets/immagine (18).png" alt=""><figcaption></figcaption></figure>

***

### Tipi di Viste

Il modulo offre tre tipi di visualizzazione principali:

#### Visualizzazione Mese

<figure><img src="../.gitbook/assets/immagine (19).png" alt=""><figcaption></figcaption></figure>

**Caratteristiche:**

* Visualizza l'intero mese in una vista a timeline
* Ogni riga rappresenta un tecnico
* Le colonne rappresentano i giorni del mese
* Ideale per una visione d'insieme

**Utilizzo:**

* Perfetto per la pianificazione a lungo termine
* Permette di identificare rapidamente i periodi di alta attività
* Utile per distribuire il carico di lavoro tra i tecnici

**Dettagli:**

* Gli eventi vengono visualizzati come barre orizzontali
* Il colore di sfondo indica lo stato dell'intervento
* Il bordo indica il tecnico assegnato (o viceversa in base alle impostazioni)
* La larghezza dell'evento indica la durata

#### Visualizzazione Settimana

<figure><img src="../.gitbook/assets/immagine (20).png" alt=""><figcaption></figcaption></figure>

**Caratteristiche:**

* Visualizza i 7 giorni della settimana
* Risoluzione oraria per ogni giorno
* Ideale per la pianificazione settimanale

**Utilizzo:**

* Perfetto per organizzare il lavoro della settimana
* Permette di vedere i dettagli orari
* Utile per evitare sovrapposizioni

**Dettagli:**

* Vista dettagliata con ore e minuti
* Possibilità di vedere la durata esatta degli interventi
* Facile identificazione dei buchi nel calendario

#### Visualizzazione Giorno

<figure><img src="../.gitbook/assets/immagine (21).png" alt=""><figcaption></figcaption></figure>

**Caratteristiche:**

* Visualizza un singolo giorno
* Massima risoluzione temporale
* Ideale per la gestione giornaliera

**Utilizzo:**

* Perfetto per la gestione operativa quotidiana
* Permette una pianificazione precisa
* Utile per gestire imprevisti e modifiche last-minute

**Dettagli:**

* Vista granulare con minuti
* Possibilità di vedere gli intervalli liberi
* Facile spostamento degli interventi

***

#### Personalizzazione della Visualizzazione

**Giorni Lavorativi**

I giorni non lavorativi vengono visualizzati con uno sfondo grigio:

* Configurabile in `Strumenti` > `Impostazioni` > `Dashboard`
* Di default: Lunedì-Venerdì
* Possibile includere/escludere la domenica

**Orario di Lavoro**

L'orario di lavoro definisce l'intervallo orario visualizzato:

* **Ora inizio**: Primo orario visibile nella vista giornaliera
* **Ora fine**: Ultimo orario visibile nella vista giornaliera
* Configurabile nelle impostazioni

**Colori degli Eventi**

I colori degli eventi seguono due modalità:

1. **Sfondo colore stato - bordo colore tecnico** (default)
   * Sfondo: colore dello stato dell'intervento
   * Bordo: colore del tecnico
2. **Sfondo colore tecnico - bordo colore stato**
   * Sfondo: colore del tecnico
   * Bordo: colore dello stato dell'intervento

Configurabile in `Strumenti` > `Impostazioni` > `Dashboard` > "Visualizzazione colori sessioni"

***

### Creazione e Modifica Attività

#### Creazione di una Nuova Attività

**Metodo 1: Clic sul Calendario**

1. **Seleziona l'intervallo di tempo**
   * Clic e trascina sul calendario per selezionare l'intervallo
   * Oppure clic su una casella vuota per un intervallo predefinito
2. **Compilazione del modulo**
   * Verrà aperto il modulo di creazione attività
   * I campi data e ora saranno precompilati
   * Il tecnico sarà selezionato in base alla riga cliccata
3. **Salvataggio**
   * Compila i campi obbligatori
   * Clicca su "Salva"
   * L'attività apparirà immediatamente nel calendario

**Metodo 2: Drag & Drop da Promemoria**

1. **Seleziona il promemoria**
   * Nella sezione "Promemoria da pianificare"
   * Trascina l'evento verso il calendario
2. **Posizionamento**
   * Rilascia l'evento nella data e ora desiderata
   * Verrà aperto il modulo di creazione con i dati precompilati
3. **Completamento**
   * Verifica i dati
   * Salva l'attività

#### Modifica di un'Attività Esistente

**Trascinamento (Spostamento)**

1. **Seleziona l'evento**
   * Clic e tieni premuto sull'evento da spostare
2. **Spostamento**
   * Trascina l'evento alla nuova posizione
   * Puoi cambiare sia data/ora che tecnico
3. **Salvataggio automatico**
   * Rilascia l'evento
   * Il sistema aggiornerà automaticamente l'attività
   * Se l'operazione non è permessa, l'evento tornerà alla posizione originale

**Ridimensionamento (Modifica Durata)**

1. **Seleziona il bordo dell'evento**
   * Posiziona il cursore sul bordo destro dell'evento
   * Il cursore cambierà forma
2. **Ridimensionamento**
   * Trascina il bordo per modificare la durata
   * Rilascia quando hai raggiunto la durata desiderata
3. **Salvataggio automatico**
   * Il sistema aggiornerà automaticamente la durata
   * Se l'operazione non è permessa, l'evento tornerà alla dimensione originale

**Modifica Dettagliata**

1. **Clic sull'evento**
   * Clicca sull'attività da modificare
   * Verrai reindirizzato alla scheda dell'intervento
2. **Modifica**
   * Modifica i campi desiderati
   * Puoi modificare tutti i dettagli dell'intervento
3. **Salvataggio**
   * Salva le modifiche
   * Il calendario si aggiornerà automaticamente

#### Visualizzazione Dettagliata

**Tooltip Informativi**

Se l'opzione "Utilizzare i tooltip sul calendario" è abilitata:

* Passa il mouse su un evento
* Verrà visualizzato un tooltip con i dettagli
* Informazioni mostrate:
  * Numero intervento
  * Data richiesta
  * Data scadenza (se presente)
  * Tipo intervento
  * Tecnici assegnati
  * Impianti coinvolti
  * Richiesta
  * Descrizione
  * Informazioni aggiuntive
  * Ragione sociale cliente
  * Telefono e cellulare
  * Indirizzo completo
  * Note anagrafica

**Accesso alla Scheda Intervento**

Cliccando su un evento:

* Verrai reindirizzato alla scheda dettagliata dell'intervento
* Da qui puoi:
  * Modificare tutti i dettagli
  * Stampare le specifiche
  * Inviare il rapportino
  * Inviare la notifica di presa in carico
  * Accedere al pannello di anteprima e firma

***

### Promemoria da Pianificare

#### Cos'è un Promemoria

Un promemoria è un intervento o attività che deve essere pianificato ma non ha ancora tecnici assegnati. Il modulo mostra due tipi di promemoria:

1. **Promemoria da Contratti**
   * Attività derivanti da contratti di manutenzione
   * Con stato pianificabile
   * Senza intervento associato
2. **Promemoria da Interventi**
   * Interventi creati ma senza tecnici assegnati
   * Con stato non bloccato
   * In attesa di assegnazione

#### Sezione Promemoria

La sezione "Promemoria da pianificare" appare se ci sono attività da pianificare:

**Struttura**

1. **Selettore Mese**
   * Permette di selezionare il mese dei promemoria da visualizzare
   * I mesi con promemoria sono elencati in ordine cronologico
2. **Lista Promemoria**
   * Ogni promemoria è mostrato come un evento trascinabile
   * Include:
     * Icona (chiave inglese per interventi, documento per contratti)
     * Nome cliente
     * Data richiesta
     * Tipo intervento
     * Descrizione della richiesta
     * Eventuali dettagli aggiuntivi
3. **Allerta Scaduti**
   * Se ci sono promemoria scaduti, appare un alert di avviso
   * Mostra il numero di promemoria scaduti

**Colori degli Eventi**

* **Blu**: Promemoria in scadenza o pianificabili
* **Rosso**: Promemoria scaduti

#### Pianificazione dei Promemoria

**Metodo 1: Drag & Drop**

1. **Seleziona il promemoria**
   * Nella sezione "Promemoria da pianificare"
   * Trascina l'evento verso il calendario
2. **Posizionamento**
   * Rilascia l'evento nella data e ora desiderata
   * Puoi anche selezionare il tecnico trascinando sulla riga corretta
3. **Creazione Intervento**
   * Verrà aperto il modulo di creazione intervento
   * I dati del promemoria saranno precompilati
   * Compila i campi mancanti e salva

**Metodo 2: Clic sul Promemoria**

1. **Clic sull'icona**
   * Clicca sull'icona a sinistra del promemoria
   * Verrai reindirizzato alla scheda di riferimento
2. **Visualizzazione dettagli**
   * Per i contratti: scheda del contratto
   * Per gli interventi: scheda dell'intervento
3. **Creazione manuale**
   * Dalla scheda, puoi creare manualmente l'intervento
   * Assegna i tecnici e pianifica l'attività

#### Filtraggio dei Promemoria

**Per Tecnico**

Se l'impostazione "Visualizza solo promemoria assegnati" è attiva:

* I tecnici vedranno solo i promemoria a loro assegnati
* Gli amministratori vedranno tutti i promemoria

**Per Mese**

Utilizza il selettore mese per:

* Visualizzare i promemoria di un mese specifico
* Pianificare le attività per il periodo desiderato
* Organizzare il lavoro in anticipo

***

### Plugin Disponibilità Tecnici

#### Descrizione

Il plugin "Disponibilità tecnici" è un componente aggiuntivo che si integra con le anagrafiche di tipo tecnico, permettendo di controllare la presenza dei tecnici nel modulo Disponibilità tecnici.

#### Accesso al Plugin

1. **Apri una scheda anagrafica**
   * Naviga in `Anagrafiche`
   * Cerca e apri la scheda di un tecnico
2. **Trova la tab**
   * Cerca la tab "Disponibilità tecnici"
   * Si trova tra le altre tabs della scheda anagrafica
3. **Accedi al plugin**
   * Clicca sulla tab per accedere al plugin



**Controllo della Visibilità**

Il plugin permette di abilitare o disabilitare la visualizzazione del tecnico nel calendario:

* **Checkbox "Visualizza in Disponibilità tecnici"**
  * Se spuntato: il tecnico appare nel calendario
  * Se deselezionato: il tecnico non appare nel calendario
  * L'impostazione viene salvata nel campo `show_disponibilita` dell'anagrafica

**Vantaggi**

* **Flessibilità**: Puoi nascondere temporaneamente tecnici senza eliminarli
* **Privacy**: Tecnici non più attivi possono essere nascosti
* **Organizzazione**: Mantieni il calendario pulito mostrando solo i tecnici attivi

***

### Aggiornamenti e Changelog

#### Versione 6.0

**Compatibilità**: OpenSTAManager 2.10.x

**Novità**:

* Introdotti file json per i controlli integrità sul modulo

#### Versione 5.1

**Compatibilità**: OpenSTAManager 2.8.2+

**Novità**:

* Miglioramenti alla visualizzazione del calendario
* Ottimizzazioni delle performance
* Correzione di bug minori

#### Versione 5.0

**Compatibilità**: OpenSTAManager 2.8+

**Novità**:

* Aggiornamento a FullCalendar v5
* Nuove viste del calendario
* Miglioramenti all'interfaccia utente
* Supporto per drag & drop migliorato

#### Versione 4.x

**Compatibilità**: OpenSTAManager 2.7+

**Novità**:

* Introduzione del plugin Disponibilità tecnici
* Miglioramenti alla gestione dei tecnici
* Nuove opzioni di personalizzazione

#### Versione 3.x

**Compatibilità**: OpenSTAManager 2.6+

**Novità**:

* Introduzione della sezione Promemoria da pianificare
* Miglioramenti alla visualizzazione degli eventi
* Correzione di bug

#### Versione 2.x

**Compatibilità**: OpenSTAManager 2.5+

**Novità**:

* Prima versione stabile
* Funzionalità base del calendario
* Integrazione con le anagrafiche

#### Versione 1.0

**Compatibilità**: OpenSTAManager 2.4+

**Novità**:

* Versione iniziale
* Funzionalità base
