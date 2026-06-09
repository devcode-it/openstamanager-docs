---
description: Guida al modulo aggiuntivo Distinta base in OpenSTAManager
---

# 📗 Distinta base

**Distinta base** è uno dei diversi moduli acquistabili da **OpenstaSTAManager.** Il modulo permette la gestione della distinta base permettendo il collegamento tra più articoli.

{% hint style="info" %}
[Clicca qui](https://shop.openstamanager.com/prodotto/distinta-base/) per procedere all'acquisto.
{% endhint %}

### Panoramica delle Funzionalità

Il plugin Distinta Base offre le seguenti funzionalità principali:

* **Gestione gerarchica delle distinte base**: Creazione di strutture ad albero con componenti e sotto-componenti
* **Produzione automatica**: Generazione di articoli finiti consumando i componenti
* **Scomposizione automatica**: Disassemblaggio di articoli finiti ripristinando i componenti
* **Controllo giacenze in tempo reale**: Verifica della disponibilità prima di operazioni di produzione/scomposizione
* **Integrazione con vendite**: Produzione automatica in fase di vendita
* **Integrazione con acquisti**: Scomposizione automatica in fase di acquisto
* **Sincronizzazione prezzi**: Aggiornamento automatico dei prezzi in base ai componenti
* **Importazione CSV**: Caricamento massivo di distinte base da file CSV
* **Stampa professionale**: Generazione di report dettagliati delle distinte base
* **Gestione multi-sede**: Supporto per diverse sedi aziendali

### Configurazione Iniziale

Dopo l'installazione, il plugin sarà disponibile nella sezione **Magazzino → Articoli**. Cliccando su un articolo, apparirà alla destra la sezione dei plugin con l'opzione "Distinta base".

<figure><img src="../.gitbook/assets/immagine (2).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/immagine (3).png" alt=""><figcaption></figcaption></figure>

#### Creazione di una Distinta Base

1. Navigare in **Magazzino → Articoli**
2. Selezionare l'articolo padre (il prodotto finito)
3. Cliccare sul plugin "Distinta base" nella colonna destra
4. Utilizzare il pulsante **+** per aggiungere componenti alla distinta

<figure><img src="../.gitbook/assets/immagine (4).png" alt=""><figcaption></figcaption></figure>

#### Configurazione dell'Articolo Padre

Per ogni articolo padre è possibile configurare le seguenti opzioni:

* **Sincronizza prezzo acquisto**: Se abilitato, il prezzo di acquisto dell'articolo padre viene aggiornato automaticamente in base ai prezzi dei componenti
* **Sincronizza prezzo vendita**: Se abilitato, il prezzo di vendita dell'articolo padre viene aggiornato automaticamente in base ai prezzi dei componenti

### Gestione della Distinta Base

#### Aggiunta di Componenti

Per aggiungere un componente alla distinta base:

1. Cliccare sul pulsante **+** nella tabella dei componenti
2. Selezionare l'articolo figlio dal campo di ricerca
3. Inserire la quantità richiesta
4. Cliccare su **Aggiungi**

Il sistema supporta la struttura gerarchica, quindi è possibile aggiungere componenti che a loro volta contengono sotto-componenti, creando distinte base multi-livello.

#### Modifica di Componenti

Per modificare un componente esistente:

1. Cliccare sull'icona **Modifica** (penna) nella riga del componente
2. Modificare la quantità desiderata
3. Cliccare su **Modifica** per salvare

#### Eliminazione di Componenti

Per rimuovere un componente dalla distinta:

1. Cliccare sull'icona **Elimina** (cestino) nella riga del componente
2. Confermare l'eliminazione

#### Visualizzazione Distinte Correlate

Se un articolo viene utilizzato come componente in altre distinte base, verrà visualizzata una sezione "Distinte in cui compare questo articolo" che mostra tutte le distinte in cui l'articolo è presente. In questa sezione è possibile modificare le quantità dell'articolo nelle diverse distinte.

#### Tabella Dettaglio Componenti

La tabella dei componenti mostra le seguenti informazioni per ogni componente:

* **Riga**: Numero progressivo del componente
* **Articolo**: Codice e descrizione dell'articolo (con link alla scheda articolo)
* **Fornitore**: Fornitore principale dell'articolo (se configurato)
* **Qta**: Quantità del componente nella distinta
* **Prezzo di acquisto**: Prezzo unitario di acquisto e totale (quantità × prezzo)
* **Prezzo di vendita**: Prezzo unitario di vendita e totale (quantità × prezzo)
* **Azioni**: Pulsanti per aggiungere, modificare o eliminare componenti

La tabella include filtri per ogni colonna per facilitare la ricerca e l'analisi dei componenti.

### Produzione e Scomposizione

Il plugin offre due operazioni principali per la movimentazione del magazzino: **Produzione** e **Scomposizione**.

<figure><img src="../.gitbook/assets/immagine (5).png" alt=""><figcaption></figcaption></figure>

#### Interfaccia Produzione/Scomposizione

La sezione "Produzione e Scomposizione" permette di:

1. Selezionare la **quantità** da produrre/scomporre
2. Selezionare la **sede** in cui effettuare l'operazione
3. Verificare in tempo reale la disponibilità dei componenti
4. Eseguire l'operazione di produzione o scomposizione

#### Controllo Giacenze

Il sistema verifica automaticamente la disponibilità quando si seleziona una sede e si inserisce una quantità:

* **Per la Produzione**: Verifica che tutti i componenti siano disponibili in quantità sufficiente
* **Per la Scomposizione**: Verifica che l'articolo padre sia disponibile in quantità sufficiente

Il controllo viene effettuato in tempo reale tramite AJAX e mostra:

* Un indicatore visivo (verde/rosso) per lo stato di disponibilità
* Il rapporto tra quantità disponibile e quantità richiesta
* Una barra di progresso per visualizzare il livello di disponibilità
* Dettagli dei componenti con problemi di disponibilità (espandibile)

#### Operazione di Produzione

La funzione **Produci** permette di creare articoli finiti consumando i componenti:

**Funzionamento:**

1. Il sistema verifica la disponibilità di tutti i componenti nella sede selezionata
2. Se i componenti sono disponibili, incrementa la quantità dell'articolo padre
3. Decrementa la quantità di tutti i componenti in base alla distinta base
4. Registra i movimenti di magazzino con causale "Produzione articolo"

**Requisiti:**

* Tutti i componenti devono essere disponibili in quantità sufficiente
* I servizi non vengono considerati nel controllo delle giacenze

**Messaggi di errore:** Se un componente non è disponibile, il sistema mostra un messaggio dettagliato con:

* Codice e descrizione del componente mancante
* Quantità disponibile
* Quantità necessaria
* Unità di misura

#### Operazione di Scomposizione

La funzione **Scomponi** permette di disassemblare articoli finiti ripristinando i componenti:

**Funzionamento:**

1. Il sistema verifica la disponibilità dell'articolo padre nella sede selezionata
2. Se l'articolo è disponibile, decrementa la quantità dell'articolo padre
3. Incrementa la quantità di tutti i componenti in base alla distinta base
4. Registra i movimenti di magazzino con causale "Scomposizione articolo"

**Requisiti:**

* L'articolo padre deve essere disponibile in quantità sufficiente

**Messaggi di errore:** Se l'articolo padre non è disponibile, il sistema mostra un messaggio dettagliato con:

* Codice e descrizione dell'articolo
* Quantità disponibile
* Quantità richiesta

#### Gestione Multi-Sede

Il plugin supporta la gestione delle giacenze in diverse sedi aziendali. È possibile:

* Selezionare la sede in cui effettuare l'operazione
* Verificare la disponibilità specifica per ogni sede
* Effettuare produzioni/scomposizioni in sedi diverse

### Integrazione con Documenti di Vendita

#### Produci articoli della distinta base in fase di vendita

L'impostazione **"Produci articoli della distinta base in fase di vendita"** permette l'esecuzione automatica dei meccanismi di composizione dell'articolo padre inserito nei documenti di vendita.

**Funzionamento:**

* L'articolo padre mantiene la sua giacenza bloccata
* Vengono movimentate le giacenze degli articoli figli (componenti)
* Al momento della vendita, vengono scalate le quantità dei componenti dal magazzino

**Caso d'uso tipico:** Un negozio di informatica che vende computer assemblati con componenti specifici. Al momento della vendita del computer, non viene ridotta la quantità dell'articolo "Computer", ma vengono scalate le quantità relative ai suoi componenti (CPU, RAM, disco, ecc.), mantenendo così allineate le giacenze.

**Considerazioni importanti:**

* Con questa impostazione abilitata è necessario monitorare attentamente le giacenze degli articoli figli
* Se le giacenze dei componenti non sono sufficienti, verranno comunque movimentate e assumeranno valori negativi
* Per evitare problemi di giacenze negative, si consiglia l'utilizzo del modulo aggiuntivo "Riordino fornitori" che permette di gestire in modo ottimale le quantità di materiale presente a magazzino

#### Configurazione

L'impostazione può essere abilitata/disabilitata dal menu **Strumenti → Impostazioni**, sezione **Distinta base**.

### Integrazione con Documenti di Acquisto

#### Scomponi articolo padre in fase di acquisto

L'impostazione **"Scomponi articolo padre in fase di acquisto"** permette di scomporre un articolo importato da una fattura di acquisto negli articoli figli che compongono la distinta.

**Funzionamento:**

* Alla registrazione di una fattura di acquisto di un articolo padre
* Viene simulata la produzione dell'articolo
* Subito dopo viene eseguita la scomposizione nei singoli componenti
* I componenti vengono registrati a magazzino

**Caso d'uso tipico:** Alla registrazione di una fattura di acquisto di una macchina, se l'impostazione è attiva, verrà simulata la produzione della macchina e subito dopo la scomposizione nei singoli componenti (motore, telaio, ruote, ecc.), che verranno registrati a magazzino.

#### Configurazione

L'impostazione può essere abilitata/disabilitata dal menu **Strumenti → Impostazioni**, sezione **Distinta base**.

### Stampa della Distinta Base

Il plugin offre una funzione di stampa professionale per generare report dettagliati delle distinte base.

#### Accesso alla Stampa

Dalla scheda dell'articolo, cliccando sul pulsante **Stampa distinta base** nella sezione configurazione, sarà possibile stampare il dettaglio della distinta.

#### Contenuti della Stampa

La stampa include:

* **Intestazione**: Codice e descrizione dell'articolo padre, data di stampa
* **Tabella dettagliata** con:
  * Riga: Numero progressivo
  * Livello: Livello di profondità nella distinta (utile per distinte multi-livello)
  * Codice: Codice dell'articolo
  * Descrizione: Descrizione dell'articolo
  * Q.tà: Quantità totale (considerando i livelli superiori)
  * U.M.: Unità di misura
  * Prezzo Acq.: Prezzo unitario di acquisto
  * Totale: Prezzo totale (quantità × prezzo)
  * Stato: Checkbox di verifica
* **Riepilogo** con:
  * Totale costo acquisto componenti
  * Totale prezzo vendita componenti
  * Margine teorico (differenza tra vendita e acquisto)

### Impostazioni del Plugin

Le impostazioni del plugin sono accessibili dal menu **Strumenti → Impostazioni**, sezione **Distinta base**.

#### Elenco delle Impostazioni

**Produci articoli della distinta base in fase di vendita**

* **Tipo**: Boolean
* **Valore predefinito**: Disabilitato
* **Descrizione**: Se abilitata, esegue automaticamente la composizione dell'articolo padre nei documenti di vendita, movimentando le giacenze degli articoli figli

**Scomponi articolo padre in fase di acquisto**

* **Tipo**: Boolean
* **Valore predefinito**: Disabilitato
* **Descrizione**: Se abilitata, scompone automaticamente l'articolo padre importato da fatture di acquisto nei componenti della distinta

**Movimenta gli articoli figlio tramite i movimenti manuali**

* **Tipo**: Boolean
* **Valore predefinito**: Disabilitato
* **Descrizione**: Se abilitata, permette la movimentazione degli articoli figlio tramite i movimenti manuali di magazzino

#### Impostazioni per Articolo

Oltre alle impostazioni globali, ogni articolo padre può avere configurazioni specifiche:

**Sincronizza prezzo acquisto**

* **Tipo**: Boolean
* **Valore predefinito**: Abilitato
* **Descrizione**: Se abilitato, aggiorna automaticamente il prezzo di acquisto dell'articolo padre in base ai prezzi dei componenti

**Sincronizza prezzo vendita**

* **Tipo**: Boolean
* **Valore predefinito**: Abilitato
* **Descrizione**: Se abilitato, aggiorna automaticamente il prezzo di vendita dell'articolo padre in base ai prezzi dei componenti

***

## Changelog

### 6.0 (2026-03-11)

#### Aggiunto (Added)

* Sistema di controlli di integrità tramite file JSON
* Funzionalità di generazione automatica dei file JSON per i controlli di integrità
* Sistema di build automatizzato con Gulp per ottimizzare lo sviluppo

### 5.1 (2025-09-24)

#### Correzioni (Fixed)

* Risolto problema nella funzionalità di stampa della distinta

### 5.0 (2025-07-23)

#### Aggiunto (Added)

* Gestione multipla delle distinte base per diverse sedi aziendali

#### Modificato (Changed)

* Migliorata l'interfaccia grafica del plugin

#### Correzioni (Fixed)

* Risolto problema nella stampa della distinta base
* Risolto problema nella visualizzazione dei dettagli dei componenti
* Risolto problema nella visualizzazione dei grafici

### 4.1 (2025-01-07)

#### Correzioni (Fixed)

* Adattato il codice per compatibilità con versioni aggiornate di PHP
* Risolto problema nella visualizzazione della descrizione degli articoli

### 4.0 (2024-11-14)

#### Correzioni (Fixed)

* Rimossi file personalizzati della classe Articolo per standardizzare il codice
* Allineata la classe Articolo con le versioni più recenti di OSM

### 3.0 (2024-06-14)

#### Aggiunto (Added)

* Aggiunto rector
* Allineamento a php8.3
* Allineamento con OSM 2.5.2

### 2.2 (2024-01-17)

#### Aggiunto (Added)

* Aggiunto php-cs-fixer
* Aggiunta colonna numero riga in distinta

### 2.1 (2023-09-05)

#### Aggiunto (Added)

* Aggiunta procedura di disintallazione del plugin
