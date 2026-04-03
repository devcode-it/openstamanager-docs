---
description: Guida al modulo aggiuntivo Vendita al banco in OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/moduli-premium/modulo-vendita-al-banco
---

# 📗 Vendita al banco

Vendita al banco è uno dei diversi moduli acquistabili da OpenSTAManager. Il modulo permette la vendita al banco di prodotti con o senza codice a barre, offrendo un'interfaccia intuitiva per la gestione delle vendite in negozio.

Per procedere all'acquisto del modulo, visitare la pagina ufficiale di OpenSTAManager.

***

### Requisiti

Il modulo Vendita al banco è compatibile con stampanti fiscali che supportano il protocollo XON/XOFF e lavorano in rete.

#### Requisiti Hardware

* Stampante fiscale con supporto protocollo XON/XOFF
* Connessione di rete per la stampante
* Lettore di codice a barre (opzionale ma consigliato)

***

### Configurazione Registratore di Cassa

Di seguito sono elencati i parametri consigliati per la configurazione del registratore di cassa:

#### Parametri Comunicazione

| Parametro              | Valore          |
| ---------------------- | --------------- |
| **Protocollo**         | XON/XOFF        |
| **Baudrate**           | 9600            |
| **Bit Number**         | \[8, NONE, 1]   |
| **XON-XOFF TX Footer** | \[DISABILITATO] |
| **XON-XOFF TX ECO**    | \[DISABILITATO] |
| **Handshake**          | \[XON/XOFF]     |
| **Modo FPU**           | \[DISABILITATO] |
| **Canale PC**          | Ethernet        |
| **Virgola inclusa**    | SI              |
| **Echo Full**          | NO              |

***

### Vendita al Banco

A seguito dell'installazione del modulo, cliccando su **Vendita al banco** apparirà la schermata principale del modulo.

<figure><img src="../.gitbook/assets/immagine (1461).png" alt=""><figcaption></figcaption></figure>

#### Creazione

Per creare una vendita al banco in OpenSTAManager:

1. Cliccare sul tasto **(+)** nella schermata principale
2. Compilare i seguenti campi:

**Campi Disponibili**

* **Stato**: Definisce lo stato della vendita (aperta/chiusa)
* **Magazzino**: Seleziona il magazzino di riferimento per la vendita
* **Pagamento**: Specifica la modalità di pagamento utilizzata
* **Cliente**: Associa la vendita a un cliente specifico
* **Agente**: Seleziona l'agente che ha effettuato la vendita
* **Registratore di cassa**: Sceglie il registratore di cassa da utilizzare
* **Importo pagato**: Indica l'importo effettivamente pagato dal cliente
* **Note**: Campo libero per eventuali annotazioni
* **Righe**: Sezione dedicata all'inserimento dei prodotti venduti

3. Inserire le righe con i prodotti venduti
4. Cliccare su **Chiudi vendita** per concludere la vendita e registrare il pagamento

<figure><img src="../.gitbook/assets/immagine (1463).png" alt=""><figcaption></figcaption></figure>

#### Modifica

Per poter modificare una vendita al banco chiusa:

1. Entrare nella vendita interessata
2. Cliccare su **Riapri vendita**
3. Apportare le modifiche necessarie
4. Chiudere nuovamente la vendita

***

### Easy Vendita

Il modulo **Easy vendita** offre un'interfaccia simile a quella di un registratore di cassa tradizionale, ottimizzata per la vendita rapida.

<figure><img src="../.gitbook/assets/immagine (1464).png" alt=""><figcaption></figcaption></figure>

#### Funzionalità Principali

**Inserimento Prodotti**

È possibile movimentare i prodotti mediante:

* **Scansione del codice a barre**: Utilizzando un lettore di codice a barre
* **Selezione dalle categorie**: Scegliendo i prodotti dalle categorie presenti in magazzino

I prodotti inseriti vengono visualizzati nella colonna di destra, dove è possibile:

* Modificare le quantità
* Modificare la riga
* Rimuovere i prodotti dal carrello

**Modifica Riga**

Cliccando su **modifica riga** si accede alla schermata di dettaglio, dove è possibile:

* Applicare uno sconto
* Cambiare l'aliquota IVA
* Modificare il prezzo di acquisto
* Modificare il prezzo di vendita

**Chiusura della Vendita**

Una volta inseriti tutti i prodotti:

1. Cliccare il tasto **PAGA**
2. Chiudere il documento
3. Procedere al pagamento
4. Stampare lo scontrino

**Selezione Registratore di Cassa**

Cliccando il pulsante **Chiusura** è possibile selezionare il registratore di cassa da cui stampare lo scontrino, tramite l'apposito menu a tendina.

**Comportamento automatico:**

* **Prima vendita**: Viene selezionato il registratore collegato alla sede dell'utente che ha effettuato l'accesso
* **Vendite successive**: Viene selezionato automaticamente l'ultimo registratore di cassa utilizzato

**Riapertura della Vendita**

Per modificare una vendita appena conclusa:

1. Cliccare su **Riapertura**
2. Apportare le modifiche necessarie
3. Chiudere nuovamente la vendita

***

### Tipologia Pagamenti

Il modulo **Tipologia pagamenti** permette di configurare le modalità di pagamento utilizzabili durante la vendita al banco.

#### Funzionalità

È possibile specificare quale tipologia di pagamento associare a una tipologia pagamenti corrispondente a un determinato codice configurato come da impostazioni del proprio registratore di cassa.

#### Utilizzo

1. Accedere al modulo Tipologia pagamenti
2. Creare o modificare una tipologia di pagamento
3. Associare il codice corrispondente alla configurazione del registratore di cassa
4. Salvare le modifiche

***

### Reparti

Il modulo **Reparti** permette di organizzare i prodotti in reparti, facilitando la gestione e la categorizzazione delle vendite.

#### Funzionalità

È possibile specificare i codici reparto da associare ai vari reparti, configurandoli come da impostazioni del proprio registratore di cassa.

#### Utilizzo

1. Accedere al modulo Reparti
2. Creare un nuovo reparto
3. Inserire il codice reparto secondo le specifiche del registratore di cassa
4. Salvare le modifiche

***

### Statistiche Vendite

Il modulo **Statistiche vendite** fornisce una visione dettagliata delle vendite al banco effettuate.

#### Funzionalità

* Visualizzazione delle statistiche delle vendite al banco
* Esploso delle righe di vendita
* Analisi dettagliata dei prodotti venduti
* Monitoraggio delle performance di vendita

#### Utilizzo

1. Accedere al modulo Statistiche vendite
2. Selezionare il periodo di interesse
3. Visualizzare i dati statistici
4. Esportare i report se necessario

***

### Registratori di Cassa

Il modulo **Registratori di cassa** permette di configurare e gestire i registratori di cassa associati al gestionale.

#### Funzionalità

* Configurazione dei registratori di cassa
* Associazione alle sedi dell'azienda
* Gestione dei parametri di connessione
* Test di connessione con le stampanti fiscali

#### Utilizzo

1. Accedere al modulo Registratori di cassa
2. Cliccare su **(+)** per aggiungere un nuovo registratore
3. Compilare i campi di configurazione:
   * Nome
   * Sede di riferimento
   * Parametri di connessione
   * Altre impostazioni specifiche
4. Salvare la configurazione
5. Testare la connessione con la stampante fiscale

***

### Plugin Reparto

Il **Plugin Reparto** è disponibile in **Strumenti > Tabelle > Categorie** e permette di gestire l'associazione massiva dei reparti alle categorie.

#### Funzionalità

È possibile impostare massivamente un reparto a tutti gli articoli presenti associati a una determinata categoria, e alle relative sottocategorie.

#### Utilizzo

1. Navigare in **Strumenti > Tabelle > Categorie**
2. Selezionare la categoria di interesse
3. Cliccare sul plugin **Reparto**
4. Selezionare il reparto da associare
5. Confermare l'operazione

#### Note Importanti

⚠️ **Attenzione**: Questa modifica influenza solo gli articoli attualmente presenti nel gestionale. Non influenza eventuali articoli inseriti in un secondo momento alla categoria.

Per applicare il reparto ai nuovi articoli, sarà necessario ripetere l'operazione o associare manualmente il reparto a ogni nuovo articolo.



## Changelog

### 8.1 (2026-03-09)

#### Corretto (Fixed)

* Correzione che verifica la quantità a magazzino dell'articolo prima di permetterne l'inserimento con impostazione sottoscorta disattivata
* Correzione generazione file JSON
* Correzione generazione file mysql.json per confronto integrità tabelle database
* Correzione minori di utilizzo
* Correzione versione

### 8.0 (2025-01-14)

#### Aggiunto (Added)

* Aggiunta generazione file JSON per verifica integrità file e database
* Aggiunta generazione modules.json per controlli database
* Aggiunta generazione settings.json per controlli database su impostazioni

#### Modificato (Changed)

* Aggiornamento versione suggerita in fase di creazione release modulo

#### Corretto (Fixed)

* Correzione query installazione
* Correzione generazione file settings.json
* Correzione generazione zip release

### 7.4 (2024-12-20)

#### Corretto (Fixed)

* Rimossa conversione indirizzo IP in numero
* Aggiunta servizi in vendita al banco
* Correzione reparto in crea vendita
* Correzione impostazione prezzi

### 7.3 (2024-12-18)

#### Corretto (Fixed)

* Correzione gestione sconto

### 7.2 (2024-12-17)

#### Ottimizzato (Refactored)

* Ottimizzazione creazione vendita

### 7.1 (2024-12-16)

#### Corretto (Fixed)

* Correzione quantità inline righe

### 7.0 (2024-12-15)

#### Aggiunto (Added)

* Miglioramento dimensione logo

#### Corretto (Fixed)

* Correzione avviso sconto
* Correzione aggiunta valore flash
* Correzione flag imponibile
* Correzione vendita banco
* Correzione allineamento tasti
* Correzione tasti per azioni rapide
* Rimozione spostamento righe
* Correzione ordinamento tasti
* Correzione posizione panel riassunto vendita
* Correzione ricerca articolo barcode
* Correzione tasto cancella righe
* Correzione reparto per descrizione
* Correzione associazione reparto a sconto
* Correzione allineamento tasto elimina
* Correzione tasti easy vendita
* Correzione aggiunta articolo
* Correzione avviso di uscita pagina
* Correzione funzione getRepartoEffettivo
* Correzione caricamento righe dopo aggiunta
* Correzione chiusura vendita easy
* Correzione vendita easy
* Modifiche vendita easy

### 6.5 (2024-11-15)

#### Aggiunto (Added)

* Aggiunta colonne Registratore di cassa e Magazzino
* Aggiunta campo idddt in vb\_venditabanco
* Migliorie vendita easy
* Miglioria minore
* Rivisitazione modulo easy vendita
* Migliorie per feedback visivo

#### Corretto (Fixed)

* Gestione reparti da categoria
* Correzione stampa vendita senza pagamento
* Correzione refuso query
* Correzione salvataggio seriali
* Correzione raggruppamento articoli per barcode
* Correzione widgets

### 6.4 (2024-10-20)

#### Aggiunto (Added)

* Gestione barcode multipli negli articoli
* Impostazione per raggruppare le righe della vendita per barcode e articolo
* Aggiunta script di creazione release

#### Corretto (Fixed)

* Correzione query di installazione
* Correzione refuso

### 6.3 (2024-10-15)

#### Aggiunto (Added)

* Indici per ottimizzazione query (idx\_vb\_venditabanco\_data, idx\_vb\_venditabanco\_deleted\_at, idx\_vb\_venditabanco\_idstato, idx\_vb\_righe\_venditabanco\_idarticolo, idx\_vb\_venditabanco\_idanagrafica, idx\_vb\_venditabanco\_data\_stato\_deleted, idx\_vb\_righe\_venditabanco\_is\_descrizione)
* Impostazione "Articoli per caricamento vendita al banco" per gestire il numero massimo di articoli da caricare per volta
* Gestione sottozero anche per ricerca tramite barcode e codice

#### Modificato (Changed)

* Migrazione impostazioni da sezione "Vendite" a "Vendita al banco"

#### Ottimizzato (Refactored)

* Miglioria caricamento articoli easy vendita

#### Corretto (Fixed)

* Introduzione caricamento limitato articoli vb easy vendita per problemi di performance
* Correzione reparto in easy vendita
* Aggiunta controllo su valore 0 nella sottocategoria dell'articolo
* Correzione impostazione
* Correzione problema apertura reparti in modifica

### 6.2 (2024-09-20)

#### Corretto (Fixed)

* Correzione impostazione reparto articoli
* Correzione creazione vendita al banco con prezzi ivati
* Correzione aggiunta riga sconto
* Correzione tasti stampa

### 6.1 (2024-09-10)

#### Aggiunto (Added)

* Allineamento 2.8

#### Corretto (Fixed)

* Correzione allineamento traduzioni
* Correzione creazione vendita al banco da attività
* Correzione buttons modulo crea vendita
* Correzione plugin Crea vendita

### 6.0 (2024-08-30)

#### Corretto (Fixed)

* Compatibilità 2.8

### 5.2 (2024-07-15)

#### Corretto (Fixed)

* Correzione: non chiude la vendita
* Fix per stampanti non abilitate al codice lotteria

### 5.1 (2024-07-10)

#### Corretto (Fixed)

* Fix minore: Aggiunta use Models\Module in vendita\_easy/row-add.php
* Fix: Correzione refuso in traduzioni (rimosso 'a' extra da "Indirizzo IP registratore di cassa") e correzione nome modulo da "Ddt di vendita" a "Ddt in uscita")

### 5.0 (2024-06-03)

#### Aggiunto (Added)

* Reso compatibile il modulo con la versione 2.5.2 beta
* Aggiunto rector
* Compatibilità con php8.3

#### Modificato (Changed)

* Aggiornamento query pagamento predefinito per mostrare tipo\_xon\_xoff
* Allineamento admin lte 3: Aggiornamento classi CSS da "box" a "card" e "checkbox" a "checkcard"

#### Corretto (Fixed)

* Fix: Correzione gestione valori null in crea\_vendita/actions.php
* Fix plugin crea vendita: Correzione recupero stati documenti e cambio stato documento in "Fatturato"
* Fix minori: Aggiornamento README, aggiunto file 5\_0.sql, aggiunto use Models\Module in vendita\_easy/edit\_articolo.php
* Fix: Correzione descrizione articolo in ajax\_articoli.php (da $articolo->descrizione a $articolo->getTranslation('title'))
* Fix: Sostituzione di `name` con `title` nelle query Module in vari file
* Fix: Correzioni query SQL in vari file di update (uso di title invece di name)
* Fix minore: Rimozione punto e virgola extra in query SQL
* Fix: Aggiunto id\_lang mancante in INSERT INTO zz\_widgets\_lang
* Fix checkbox: Sostituzione di type="checkcard" con type="checkbox" in crea\_vendita/crea\_documento.php
* Fix menu dropdown
* Fix: Aggiunta header file PHP in tutti i file vendita\_easy
* Fix: Aggiornamento query per compatibilità con traduzioni (uso di getTranslation, title al posto di name)
* Fix: Correzione query update per widget e moduli (uso di zz\_modules\_lang per recuperare id)
* Fix: Aggiornamento query update 4\_0.sql per gestione views\_lang
* Fix: Aggiunta header file PHP in vendita\_easy
* Fix: Correzione descrizione articolo e query categorie per traduzioni
* Fix: Aggiornamento query per pagamenti e segmenti con supporto traduzioni
* Fix: Rimozione file update vendita\_easy non più necessari
* Allineamento modulo con release 2.5 beta

### 4.2 (2024-01-16)

#### Aggiunto (Added)

* Aggiunto php-cs-fixer

### 4.1 (2023-12-14)

#### Aggiunto (Added)

* Aggiunta visualizzazione dati bancari in template di stampa

#### Corretto (Fixed)

* Corretta la chiusura della stampa
* Fix

### 4.0 (2023-12-05)

#### Aggiunto (Added)

* Aggiunta la gestione dei seriali
* Aggiunta gestione di registratori di cassa multipli associati alle sedi

#### Corretto (Fixed)

* Corretta la stampa e chiusura della vendita-easy
* Fix installazione

### 3.1 (2023-10-24)

#### Corretto (Fixed)

* Corretta la stampa e chiusura della vendita-easy
* Fix sconto predefinito
* Fix easy vendita
* Allineamento metodi di pagamento standard

### 2.1.4 (2023-08-03)

#### Corretto (Fixed)

* Corretto il salvataggio del numero di una vendita al banco
