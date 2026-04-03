---
description: Guida al modulo aggiuntivo Registrazione movimenti bancari di OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/moduli-premium/registrazione-movimenti-bancari
---

# 📗 Registrazione movimenti bancari

**Registrazione movimenti bancari** è un modulo acquistabile da **OpenstaSTAManager.** Il modulo permette di importare i movimenti bancari e registrarli direttamente in prima nota.

### Funzionalità Principali

#### 1. Importazione Movimenti Bancari

Il modulo permette di importare i movimenti bancari tramite file CSV, solitamente forniti direttamente dalla propria banca.

**Procedura di importazione:**

1. Accedere a **Strumenti > Import**
2. Cliccare sul pulsante **(+)** per aggiungere una nuova importazione
3. Selezionare **Prima nota** nel menu a tendina
4. Cliccare su **Scarica esempio CSV** per scaricare un file di esempio da seguire per configurare correttamente i campi del file da importare

**Formato del file CSV**

Il file CSV deve contenere i seguenti campi:

**Opzione 1 - Con colonne Dare e Avere:**

* Data Contabile
* Descrizione
* Dare
* Avere
* Causale ABI (facoltativo)

**Opzione 2 - Con colonna Importo:**

* Data Contabile
* Descrizione
* Importo
* Causale ABI (facoltativo)

Esempio di formato:

```csv
Data Contabile,Descrizione,Dare,Avere,Causale ABI(facoltativo)
01/01/2021,Pagamento fattura n.1 del...,0,10,1
```

Oppure:

```csv
Data Contabile,Descrizione,Importo,Causale ABI(facoltativo)
01/01/2021,Pagamento fattura n.1 del...,-10,1
```

<figure><img src="../.gitbook/assets/immagine (567).png" alt=""><figcaption></figcaption></figure>

#### 2. Visualizzazione e Gestione Movimenti

Una volta importato il file CSV, verrà visualizzata la lista di tutti i movimenti con le seguenti informazioni:

* **Data**: data del movimento bancario
* **Descrizione**: descrizione del movimento
* **Importo**: importo del movimento (in verde per entrate, in rosso per uscite)
* **Anteprima**: anteprima dei conti che verranno utilizzati per la registrazione
* **Scadenza**: menu a tendina per selezionare la relativa scadenza
* **Azioni**: pulsanti per registrare o ignorare il movimento

**Informazioni aggiuntive**

Nella parte superiore della pagina sono visualizzate due informazioni importanti:

* **Ultimo movimento processato**: data dell'ultimo movimento che è stato registrato in prima nota
* **Ultimo movimento importato**: data dell'ultimo movimento importato ma non ancora processato

#### 3. Selezione Banca

Prima di procedere con la registrazione dei movimenti, è necessario selezionare la banca da utilizzare:

1. Utilizzare il campo **Banca** in alto a destra
2. Selezionare la banca desiderata dal menu a tendina
3. La banca verrà utilizzata per determinare il conto bancario da utilizzare nelle registrazioni

La selezione della banca viene memorizzata in sessione per le successive operazioni.

#### 4. Associazione Scadenze

Per ogni movimento importato, è possibile associare una o più scadenze:

**Selezione manuale:**

* Utilizzare il menu a tendina **Scadenza** per selezionare manualmente le scadenze da associare
* È possibile selezionare più scadenze per un singolo movimento
* Le scadenze mostrano informazioni dettagliate:
  * Nome anagrafica (cliente/fornitore)
  * Numero fattura e data
  * Importo residuo
  * Data scadenza
  * Numero di solleciti inviati (se presenti)
  * Tipo pagamento

**Autocompletamento automatico:**

* Cliccare sul pulsante con l'icona magica (🪄) per tentare l'autocompletamento automatico
* Il sistema cercherà le scadenze che corrispondono all'importo del movimento
* La ricerca viene effettuata in un intervallo di 7 giorni prima della data del movimento

**Compilazione automatica:**

* Utilizzare il pulsante **Compila** (se disponibile) per compilare automaticamente tutte le scadenze
* Il sistema associa automaticamente le scadenze in base a diversi criteri:
  * Corrispondenza esatta dell'importo
  * Corrispondenza dell'importo con l'aggiunta delle commissioni bancarie
  * Match tramite pattern definiti nei modelli (es. ricerca di distinta nella descrizione)
  * Algoritmo di combinazione per trovare la migliore combinazione di scadenze

#### 5. Anteprima Movimenti

Per ogni movimento, è possibile visualizzare l'anteprima dei conti che verranno utilizzati per la registrazione:

* L'anteprima viene visualizzata automaticamente quando si seleziona una scadenza
* Mostra i movimenti in **Dare** (in verde con freccia su) e **Avere** (in rosso con freccia giù)
* Include eventuali commissioni bancarie
* Mostra una barra di progresso che indica quanto dell'importo del movimento è coperto dalle scadenze selezionate
* Se l'importo totale corrisponde, la barra è verde; altrimenti è arancione

**Tipi di anteprima:**

1. **Anteprima da scadenze**: mostra i conti cliente/fornitore e il conto bancario
2. **Anteprima da modello**: utilizza i conti definiti in un modello di prima nota
3. **Anteprima giroconto**: mostra i conti per i movimenti di giroconto tra conti bancari

#### 6. Registrazione Movimenti

**Registrazione singola:**

1. Selezionare le scadenze da associare al movimento
2. Verificare l'anteprima dei movimenti
3. Cliccare sul pulsante **Registra** (icona €)
4. Verrà aperta una finestra modale con i dettagli della registrazione
5. Verificare e modificare se necessario:
   * Data movimento
   * Causale
   * Conti da utilizzare
6. Cliccare su **Aggiungi** per confermare la registrazione in prima nota

**Registrazione con modello:**

Se è presente un modello di prima nota associato:

1. Selezionare il modello dal menu a tendina
2. I conti verranno automaticamente compilati secondo il modello
3. È possibile modificare i conti se necessario
4. Cliccare su **Aggiungi e crea modello** per salvare un nuovo modello
5. Cliccare su **Aggiungi e modifica modello** per aggiornare il modello esistente

**Registrazione massiva:**

1. Selezionare i movimenti da registrare utilizzando le checkbox
2. Cliccare su **Azioni di gruppo** > **Registra anteprima movimento**
3. Confermare l'operazione
4. I movimenti selezionati verranno registrati automaticamente utilizzando le anteprime

#### 7. Gestione Commissioni Bancarie

Il modulo gestisce automaticamente le commissioni bancarie in diversi modi:

**Rilevamento automatico:**

* Cerca pattern specifici nella descrizione del movimento (es. "COMM.NI 1,50")
* Se rileva una commissione, la scorpora automaticamente dall'importo totale

**Gestione manuale:**

* Se l'importo delle scadenze è inferiore all'importo del movimento, la differenza viene considerata come commissione
* Le commissioni vengono registrate su:
  * Conto bancario
  * Conto spese (configurabile nelle impostazioni)

**Configurazione:**

È possibile configurare i modelli per la gestione delle commissioni:

* Definire il pattern per rilevare le commissioni nella descrizione
* Specificare il conto bancario da utilizzare
* Specificare il conto spese da utilizzare

#### 8. Ignorare Movimenti

Per rimuovere un movimento dalla lista senza registrarlo:

1. Cliccare sul pulsante **X** (icona croce) accanto al pulsante Registra
2. Confermare l'operazione
3. Il movimento verrà marcato come processato e non verrà più visualizzato

#### 9. Rimozione Massiva

Per rimuovere tutti i movimenti importati ma non processati:

1. Cliccare sul pulsante **Rimuovi movimenti** in alto a destra
2. Confermare l'operazione
3. Tutti i movimenti non processati verranno rimossi

### Modulo Movimenti ABI

Il modulo include anche una sezione "Movimenti ABI" che permette di gestire i codici ABI (Associazione Bancaria Italiana) e associarli a modelli di prima nota.

#### Funzionalità:

1. **Visualizzazione movimenti ABI**: lista dei codici ABI configurati con descrizione
2. **Aggiunta movimento ABI**: permette di aggiungere nuovi codici ABI
3. **Modifica movimento ABI**: permette di modificare i codici ABI esistenti e associarli a un modello
4. **Eliminazione movimento ABI**: permette di rimuovere i codici ABI non più utilizzati

#### Utilizzo:

I codici ABI vengono utilizzati durante l'importazione dei movimenti bancari:

* Se il file CSV contiene una colonna "Causale ABI", il sistema cerca il corrispondente codice ABI
* Se trovato, viene utilizzato il modello associato per generare l'anteprima dei movimenti
* Questo permette di automatizzare la registrazione di movimenti ricorrenti (es. stipendi, pagamenti fornitori, ecc.)

<figure><img src="../.gitbook/assets/immagine (862).png" alt=""><figcaption></figcaption></figure>

### Modelli di Prima Nota

Il modulo permette di creare e utilizzare modelli di prima nota per automatizzare la registrazione di movimenti ricorrenti.

#### Tipi di modelli:

1. **Preview**: modello utilizzato per generare l'anteprima dei movimenti basandosi su pattern nella descrizione
2. **Giroconto**: modello utilizzato per i movimenti di giroconto tra conti bancari
3. **Commissioni**: modello utilizzato per gestire automaticamente le commissioni bancarie
4. **Search**: modello utilizzato per cercare corrispondenze con le scadenze tramite pattern (es. distinta)
5. **Autocomplete**: modello utilizzato per l'autocompletamento automatico delle scadenze

#### Creazione di un modello:

1. Durante la registrazione di un movimento, cliccare su **Aggiungi e crea modello**
2. Il sistema salverà la configurazione dei conti utilizzati come nuovo modello
3. Il modello potrà essere riutilizzato per movimenti simili

#### Utilizzo dei modelli:

I modelli vengono applicati automaticamente in base a:

* Codice ABI presente nel movimento
* Pattern nella descrizione del movimento
* Tipo di movimento (giroconto, commissioni, ecc.)

### Configurazione

#### Impostazioni principali:

* **Conto aziendale predefinito**: conto utilizzato se non è specificata una banca
* **Conto predefinito per commissioni**: conto utilizzato per registrare le commissioni bancarie
* **Conto anticipo clienti**: conto utilizzato per gestire gli anticipi dai clienti
* **Conto anticipo fornitori**: conto utilizzato per gestire gli anticipi ai fornitori

#### Configurazione modelli:

È possibile configurare i modelli di prima nota per automatizzare la registrazione:

1. Accedere a **Prima nota > Modelli**
2. Creare o modificare un modello
3. Definire:
   * Nome del modello
   * Descrizione/Causale
   * Conti da utilizzare (con possibilità di utilizzare placeholder)
   * Opzioni specifiche (tipo di modello, pattern, ecc.)

***

### Changelog

#### 6.0 (2026-03-17)

**Aggiunto (Added)**

* File JSON per controlli integrità
* Allineamento per versione 2.10
* Gestione file JSON per controlli di integrità
* Gulpfile e package.json per automazione build

**Modificato (Changed)**

* Migliorie grafiche

#### 5.3 (2025-07-28) - Release Precedente

**Aggiunto (Added)**

* Tipo pagamento in lista scadenze

#### 5.2 (2025-06-25)

**Aggiunto (Added)**

* Migliorata visualizzazione date importazioni
* Data di ultimo movimento processato

**Corretto (Fixed)**

* Importazione massiva
* Problema importazione importi negativi

#### 5.1 (2025-03-11)

**Corretto (Fixed)**

* Allineamento versione 2.7.\*
* Autocompletamento scadenze

#### 5.0 (2025-01-28)

**Corretto (Fixed)**

* Allineamento

#### 4.1 (2024-12-02)

**Aggiunto (Added)**

* Modulo import movimenti + esempio

**Corretto (Fixed)**

* Ripristinato pulsante azioni di gruppo
* Correzione codice
* Query aggiornamento
* Rimozione modulo import movimenti
* Aggiornamenti e fix modulo registra movimenti
* Associazione fattura

#### 4.0 (2024-10-10)

**Aggiunto (Added)**

* Modelli per collegamento scadenze tramite match distinta e anteprime movimenti

**Modificato (Changed)**

* Pre-selezione banca da banca presente nel modulo

**Corretto (Fixed)**

* Allineamento PHP 8.3
* File update
* Fix minori

#### 3.1 (2024-01-17)

**Modificato (Changed)**

* Migliorie modulo registra movimento

**Corretto (Fixed)**

* Data movimento
* Causale movimento

#### 3.0 (2023-10-13)

**Corretto (Fixed)**

* Importazione
* PHP 8
* Segni movimenti

#### 2.0 (2023-06-05)

**Modificato (Changed)**

* Allineamento versione 2.4.46

#### 1.0 (2022-11-28)

**Corretto (Fixed)**

* Aggiungi e crea modello

#### Videoguida:

{% content-ref url="../guide/videoguide/registrazione-movimenti-bancari.md" %}
[registrazione-movimenti-bancari.md](../guide/videoguide/registrazione-movimenti-bancari.md)
{% endcontent-ref %}
