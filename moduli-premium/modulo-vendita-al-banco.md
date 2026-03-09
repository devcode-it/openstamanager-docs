---
description: Guida al modulo aggiuntivo Vendita al banco in OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/I8PynmXUVfCOtwZFC1I6/moduli-premium/modulo-vendita-al-banco
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

<figure><img src="../.gitbook/assets/immagine (1443).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../.gitbook/assets/immagine (1445).png" alt=""><figcaption></figcaption></figure>

#### Modifica

Per poter modificare una vendita al banco chiusa:

1. Entrare nella vendita interessata
2. Cliccare su **Riapri vendita**
3. Apportare le modifiche necessarie
4. Chiudere nuovamente la vendita

***

### Easy Vendita

Il modulo **Easy vendita** offre un'interfaccia simile a quella di un registratore di cassa tradizionale, ottimizzata per la vendita rapida.

<figure><img src="../.gitbook/assets/immagine (1446).png" alt=""><figcaption></figcaption></figure>

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
