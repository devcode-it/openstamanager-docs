---
description: Guida al modulo aggiuntivo Presenze di OpenSTAManager
metaLinks:
  alternates:
    - https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/moduli-premium/presenze
---

# 📗 Presenze

**Presenze** è un modulo acquistabile da **OpenstaSTAManager.** Il modulo permette di programmare le attività dei tecnici in base alle ore di lavoro giornaliere.

#### Caratteristiche Principali

* Gestione sessioni di lavoro per tecnici
* Supporto per diversi tipi di sessioni (ordinarie, straordinarie, notturne, ferie, permessi, malattia)
* Visualizzazione calendario mensile con colorazione automatica
* Gestione multipla delle sessioni
* Stampa del foglio presenze
* Calcolo automatico delle ore straordinarie
* Rilevamento sovrapposizioni tra sessioni
* Integrazione completa con il modulo Interventi

### Configurazione Iniziale

Prima di poter utilizzare il modulo Presenze, è necessario completare la seguente configurazione:

#### 1. Configurazione Anagrafica Azienda

L'anagrafica azienda deve avere il tipo "Cliente" oltre ad "Azienda":

1. Accedere a **Anagrafiche**
2. Aprire l'anagrafica dell'azienda
3. Verificare che il tipo "Cliente" sia presente
4. Se non presente, aggiungere il tipo "Cliente" all'anagrafica azienda

<figure><img src="../.gitbook/assets/immagine (1284).png" alt=""><figcaption></figcaption></figure>

#### 2. Creazione Attività Fittizia

È necessario creare un'attività fittizia associata all'anagrafica azienda:

1. Accedere al modulo **Attività**
2. Creare una nuova attività
3. Impostare come cliente l'anagrafica azienda
4. Salvare l'attività
5. Annotare il codice dell'attività creato

<figure><img src="../.gitbook/assets/immagine (1285).png" alt=""><figcaption></figcaption></figure>

#### 3. Configurazione Tipi di Attività

Configurare i tipi di attività con le relative tariffe orarie:

1. Accedere a **Attività > Tipi di attività**
2. Creare o modificare i seguenti tipi:
   * **Sessione ordinaria**: per le ore di lavoro standard
   * **Sessione notturna**: per il lavoro notturno
   * **Ferie**: per i giorni di ferie
   * **Permesso**: per i permessi retribuiti
   * **Malattia**: per i giorni di malattia

<figure><img src="../.gitbook/assets/immagine (1292).png" alt=""><figcaption></figcaption></figure>

#### 4. Configurazione Impostazioni del Modulo

Accedere a **Strumenti > Impostazioni** e configurare le seguenti impostazioni nella sezione "Presenze":

* **Tipologia intervento per conteggio notturni**
* **Tipologia intervento per conteggio ferie**
* **Tipologia intervento per conteggio permessi**
* **Tipologia intervento per conteggio malattie**
* **Ore minime di lavoro:** ore minime lavorate per colorare la riga di verde nel modulo Presenze
* **Codice intervento da utilizzare per attività fittizia:** andrà qui selezionata l'attività creata precedentemente

Ora che il modulo è stato configurato, sarà possibile accedervi e selezionare i tecnici per gestire le ore di lavoro:

<figure><img src="../.gitbook/assets/immagine (1289).png" alt=""><figcaption></figcaption></figure>

Dopo aver completato la configurazione, accedere al modulo **Presenze**. Se tutte le impostazioni sono state configurate correttamente, il modulo mostrerà l'interfaccia principale. In caso contrario, verrà visualizzato un messaggio di avviso:

```
⚠️ Configurare tutte le impostazioni della sezione "Presenze" per utilizzare il modulo
```

### Funzionalità Principali

#### 1. Visualizzazione Calendario Mensile

Il modulo presenta un'interfaccia calendario mensile con le seguenti caratteristiche:

**Organizzazione per Mesi**

* **Navigazione**: Tab per selezionare il mese desiderato
* **Periodo**: Il periodo di visualizzazione è definito dalle impostazioni di sessione (period\_start e period\_end)
* **Mese Corrente**: Il mese corrente viene evidenziato automaticamente

**Colorazione delle Righe**

Le righe della tabella vengono colorate in base allo stato del giorno:

* **🟢 Verde**: Giorno lavorativo con ore totali ≥ ore minime di lavoro
* **🔴 Rosso**: Giorno non lavorativo (weekend o festivo)
* **🔵 Blu**: Giorno con evento generico
* **⚪ Bianco/Grigio**: Giorno lavorativo con ore totali < ore minime di lavoro

**Gestione Eventi**

Il modulo integra automaticamente gli eventi dal sistema:

* **Eventi Festivi**: Vengono mostrati con badge rosso e il nome dell'evento
* **Eventi Ricorrenti**: Gli eventi ricorrenti vengono considerati automaticamente
* **Eventi Generici**: Vengono mostrati con badge blu

#### 2. Calcolo Automatico delle Ore

Il modulo calcola automaticamente le diverse tipologie di ore:

**Ore Ordinarie**

* Vengono calcolate fino al limite delle "Ore minime di lavoro"
* Le ore oltre questo limite vengono automaticamente convertite in straordinarie
* **Formula**: `min(ore_totali, ore_minime_lavoro)`

**Ore Straordinarie**

* Vengono calcolate solo se le ore ordinarie superano le ore minime
* **Formula**: `max(0, ore_totali - ore_minime_lavoro)`

**Ore Speciali**

Le ore speciali (notturne, ferie, permessi, malattia) vengono calcolate in base al tipo di intervento associato alla sessione:

* **Notturne**: Sessioni con tipo intervento configurato come "notturno"
* **Ferie**: Sessioni con tipo intervento configurato come "ferie"
* **Permessi**: Sessioni con tipo intervento configurato come "permesso"
* **Malattia**: Sessioni con tipo intervento configurato come "malattia"

<figure><img src="../.gitbook/assets/immagine (1288).png" alt=""><figcaption></figcaption></figure>

#### 3. Rilevamento Sovrapposizioni

Il modulo rileva automaticamente le sovrapposizioni tra sessioni dello stesso giorno:

**Logica di Rilevamento**

* Confronta tutte le coppie di sessioni del giorno
* Calcola l'intervallo di sovrapposizione
* Assegna la sovrapposizione alla sessione che inizia per seconda
* Per due sessioni ordinarie sovrapposte, la sovrapposizione viene assegnata alle "straordinarie"

**Visualizzazione delle Sovrapposizioni**

* Viene mostrato un avviso con icona ⚠️
* Il tooltip mostra i dettagli delle sessioni sovrapposte
* Vengono indicate le ore di sovrapposizione per ogni tipo

<figure><img src="../.gitbook/assets/immagine (1293).png" alt=""><figcaption></figcaption></figure>

#### 4. Totali Mensili

In fondo alla tabella vengono mostrati i totali del mese:

* **Totale Ordinarie**: Somma delle ore ordinarie del mese
* **Totale Straordinarie**: Somma delle ore straordinarie del mese
* **Totale Notturni**: Somma delle ore notturne del mese
* **Totale Ferie**: Somma delle ore di ferie del mese
* **Totale Permessi**: Somma delle ore di permesso del mese
* **Totale Malattia**: Somma delle ore di malattia del mese
* **Totale Generale**: Somma di tutte le ore del mese

### Utilizzo del Modulo

#### Accesso al Modulo

1. Accedere al menu principale di OpenSTAManager
2. Selezionare il modulo **Presenze**
3. Verrà mostrata la lista dei tecnici configurati come "Tecnico"

#### Selezione del Tecnico

1. Selezionare il tecnico desiderato dalla lista
2. Verrà mostrata l'interfaccia principale con il calendario mensile

#### Informazioni del Tecnico

Nella parte superiore dell'interfaccia vengono mostrate le informazioni del tecnico:

* **Foto**: Se presente, viene mostrata la foto profilo dell'utente
* **Nome**: Ragione sociale del tecnico
* **Descrizione**: "Presenze e sessioni di lavoro"

#### Navigazione tra i Mesi

1. Utilizzare i tab nella parte superiore per selezionare il mese desiderato
2. Il mese corrente viene evidenziato automaticamente
3. È possibile navigare tra i mesi all'interno del periodo definito

***

### Gestione delle Sessioni

#### Creazione di una Nuova Sessione

**Sessione Ordinaria**

1. Selezionare il giorno desiderato
2. Inserire l'orario di inizio (default: orario lavorativo standard)
3. Inserire l'orario di fine (default: calcolato automaticamente)
4. Aggiungere eventuali note
5. Cliccare sul pulsante **"Ordinaria"**

**Sessione Speciale**

1. Selezionare il giorno desiderato
2. Inserire l'orario di inizio
3. Inserire l'orario di fine
4. Aggiungere eventuali note
5. Cliccare sulla freccia del pulsante **"Ordinaria"**
6. Selezionare il tipo di sessione desiderato:
   * **🌙 Sessione notturna**
   * **☀️ Ferie**
   * **⏸️ Permesso**
   * **🏥 Malattia**

**Suggerimento Automatico degli Orari**

Il modulo suggerisce automaticamente gli orari in base:

* **Orario Standard**: Utilizza gli orari "Inizio orario lavorativo" e "Fine orario lavorativo" dalle impostazioni
* **Sessioni Esistenti**: Se ci sono già sessioni nel giorno, suggerisce di iniziare dopo l'ultima sessione
* **Ore Rimanenti**: Calcola le ore rimanenti per raggiungere le ore minime di lavoro

#### Modifica delle Sessioni

**Modifica Singola Sessione**

1. Cliccare sul totale delle ore nella colonna **"Totale"**
2. Verrà aperto il modale **"Modifica sessioni"**
3. Modificare gli orari di inizio/fine delle sessioni
4. Le ore vengono ricalcolate automaticamente
5. Chiudere il modale per salvare le modifiche

**Eliminazione Sessione**

1. Aprire il modale **"Modifica sessioni"**
2. Cliccare sull'icona 🗑️ accanto alla sessione da eliminare
3. Confermare l'eliminazione

#### Gestione Multipla delle Sessioni

Il modulo permette di creare sessioni multiple in un'unica operazione:

**Accesso alla Gestione Multipla**

1. Cliccare sul pulsante **"Gestione multipla"** in fondo alla tabella
2. Verrà aperto il modale **"Gestione multipla sessioni"**

**Configurazione della Gestione Multipla**

**Orari**

* **Ora inizio**: Orario di inizio delle sessioni (default: 08:00)
* **Ora fine**: Orario di fine delle sessioni (default: 18:00)

**Periodo**

* **Data inizio**: Prima data per cui creare le sessioni (default: primo del mese corrente)
* **Data fine**: Ultima data per cui creare le sessioni (default: ultimo del mese corrente)

**Giorni**

* **Giorni**: Selezionare i giorni della settimana in cui creare le sessioni (default: giorni lavorativi)
* **Tipo sessione**: Selezionare il tipo di sessione da creare:
  * Ordinaria
  * Notturna
  * Ferie
  * Permesso
  * Malattia

**Note**

* **Note**: Aggiungere eventuali note per le sessioni

**Opzioni**

* **Sovrascrivi sessioni esistenti**: Se selezionato, sostituisce le sessioni esistenti
* **Escludi giorni festivi**: Se selezionato, non crea sessioni nei giorni festivi

**Esecuzione della Gestione Multipla**

1. Configurare tutti i parametri desiderati
2. Cliccare sul pulsante **"Crea sessioni"**
3. Il modulo creerà le sessioni secondo i parametri configurati
4. Verrà mostrato un messaggio con il numero di sessioni create

***

### Stampa delle Presenze

Il modulo permette di generare un report stampabile delle presenze.

#### Accesso alla Stampa

**Stampa Singolo Tecnico**

1. Selezionare il tecnico desiderato
2. Cliccare sull'icona della stampante nella barra degli strumenti
3. Selezionare il mese desiderato
4. Verrà generato il PDF del foglio presenze

**Stampa Multipla Tecnici**

1. Selezionare più tecnici dalla lista (checkbox)
2. Cliccare sul pulsante **"Stampa presenze"** nel menu azioni
3. Selezionare il mese desiderato
4. Verrà generato il PDF con le presenze di tutti i tecnici selezionati

#### Formato del Report

Il report PDF ha le seguenti caratteristiche:

**Impostazioni di Pagina**

* **Orientamento**: Orizzontale (Landscape)
* **Formato**: A4
* **Dimensione font**: 9pt
* **Margini**: 10mm (alto/basso), 5mm (sinistra/destra)

**Struttura del Report**

* **Intestazione**: Nome dell'azienda
* **Titolo**: Nome del mese e anno
* **Tabella**: Una riga per ogni tecnico con le seguenti sottorighe:
  * Ore ordinarie
  * Ore straordinarie
  * Ore notturne
  * Ferie
  * Permessi
  * Malattia
  * Totale

**Colorazione**

* **Rosso**: Giorni non lavorativi (weekend o festivi)
* **Blu**: Giorni con eventi generici
* **Nero**: Giorni lavorativi normali

***

### Changelog

#### 3.0 (2026-03-17)

**Aggiunte**

* File JSON per controlli integrità del modulo
* Gestione file JSON per controlli integrità
* Strumento Rector per refactoring automatico del codice
* Gulpfile e package.json per automazione build e sviluppo

**Correzioni**

* Allineamento versione 2.10
* File .gitignore aggiornato per escludere file non necessari

#### 2.0 (2025-07-23)

**Aggiunte**

* Gestione presenze multiple per elaborazione in blocco

#### 1.2 (2025-07-14)

**Aggiunte**

* Miglioramento stampa e orari per inserimento sessioni presenze
* Filtro per stati da utilizzare nel calcolo delle presenze

**Correzioni**

* Correzione link all'attività

#### 1.1 (2025-04-09)

**Correzioni**

* Eliminazione sessioni

#### 1.0 (2024-11-15)

**Aggiunte**

* Prima versione del modulo presenze

***

### Supporto e Contatti

Per supporto tecnico, segnalazioni di bug o richieste di funzionalità:

* **Sviluppatore**: DevCode s.r.l.
* **Licenza**: GPL-3.0
* **Documentazione**: https://docs.openstamanager.com
* **Community**: https://community.openstamanager.com

***

### Note Legali

Questo modulo è rilasciato sotto licenza GPL-3.0. È consentito l'utilizzo, la modifica e la distribuzione del modulo secondo i termini della licenza.

Il modulo è compatibile con OpenSTAManager versione 2.8.0 e successive.

***

_Ultimo aggiornamento: 17 Marzo 2026_ _Versione documento: 1.0_
