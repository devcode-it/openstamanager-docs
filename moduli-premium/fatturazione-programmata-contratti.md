---
description: >-
  Guida al modulo aggiuntivo Fatturazione programmata contratti in
  OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/imnORsInuaaXiiRnlr6m/moduli-premium/fatturazione-programmata-contratti
---

# 📗 Fatturazione programmata contratti

{% hint style="info" %}
Il modulo **Fatturazione programmata contratti** permette di pianificare la rateizzazione di un contratto impostando l'emissione automatica di una fattura di vendita e invio via email della copia di cortesia al cliente.
{% endhint %}

#### Caratteristiche principali

* **Pianificazione flessibile**: Imposta liberamente la ricorrenza di fatturazione, la data di inizio e l'importo di ogni rata
* **Automazione completa**: Configurazione di script in cron per fatturazione automatica, invio XML allo SDI e invio email
* **Vista mensile**: Visualizzazione generica suddivisa per mese di tutte le rate in scadenza
* **Fatturazione massiva**: Possibilità di fatturare massivamente le rate tramite azione di gruppo
* **Filtri avanzati**: Filtraggio per contratto, cliente, data e pagamento
* **Cadenza anticipata/posticipata**: Gestione delle rate con generazione anticipata o posticipata

### Configurazione

Dopo l'installazione del modulo, in **Strumenti > Impostazioni** nella sezione **Contratti** sarà possibile trovare le seguenti impostazioni:

#### Descrizione righe nella fatturazione dei contratti

**Tipo**: Stringa\
**Descrizione**: Definisce il formato che avranno le righe della fattura generata tramite automatismo.

**Variabili disponibili**:

* `{ragione_sociale}`: Ragione sociale del cliente
* `{nome}`: Nome del contratto
* `{data}`: Data della fatturazione
* Altre variabili definite nel file `custom/variables.php` del modulo Contratti

**Esempio**:

```
Canone mensile per contratto {nome} - Periodo {data}
```

#### Cron fatturazione

**Tipo**: Lista\
**Opzioni disponibili**:

* `Crea in bozza`: Crea le fatture in stato Bozza
* `Emetti fattura`: Crea le fatture e le emette immediatamente
* `Emetti ed invia PDF`: Crea le fatture, le emette e invia la copia PDF via email
* `Emetti ed invia PDF e XML`: Crea le fatture, le emette, invia la copia PDF via email e genera l'XML per l'invio allo SDI

**Descrizione**: Scegliere gli automatismi da eseguire durante l'esecuzione dello script cron.

#### Elaborazione invio automatico XML

**Tipo**: Intero\
**Valore predefinito**: 10\
**Descrizione**: Definisce i giorni di ritardo dall'emissione dell'XML al suo invio allo SDI, per permettere la sua eventuale modifica. Se al documento venisse variato lo stato entro i giorni stabiliti, l'automatismo viene interrotto e occorrerà inviare il file manualmente.

**Esempio**: Se impostato a 10, l'XML verrà inviato allo SDI 10 giorni dopo la generazione della fattura.



***

### Utilizzo del modulo

#### Accesso al modulo

Il modulo è accessibile dal menu principale di OpenSTAManager:

1. Navigare in **Contratti**
2. Selezionare **Fatturazione contratti**

#### Interfaccia principale

L'interfaccia principale mostra una vista mensile di tutte le rate in scadenza, organizzate in schede per mese e anno.

**Filtri disponibili**

* **Cliente**: Filtra per anagrafica cliente
* **Contratto**: Filtra per nome del contratto
* **Data**: Filtra per giorno di inizio fatturazione
* **Pagamento**: Filtra per metodo di pagamento

**Visualizzazione delle rate**

Per ogni mese, vengono visualizzate le seguenti informazioni:

| Colonna         | Descrizione                          |
| --------------- | ------------------------------------ |
| Checkbox        | Per selezionare le rate da fatturare |
| Scadenza rata   | Data della scadenza della rata       |
| Contratto       | Link al contratto                    |
| Ragione sociale | Nome del cliente                     |
| Pagamento       | Metodo di pagamento                  |
| Sede            | Sede di destinazione (o Sede legale) |
| Descrizione     | Descrizione della rata               |
| Totale          | Importo imponibile della rata        |
| Totale scadenza | Importo totale comprensivo di IVA    |

#### Azioni disponibili

**Seleziona tutto per mese**

Per ogni mese è presente un checkbox "Seleziona tutto" che permette di selezionare tutte le rate del mese.

**Crea fattura**

Permette di creare fatture per le rate selezionate:

1. Selezionare le rate da fatturare
2. Cliccare su **Crea fattura**
3. Nella modale che appare, configurare:
   * **Accodare**: Se selezionato, le rate vengono accodate a fatture esistenti in stato Bozza per lo stesso cliente
   * **Sezionale**: Sezionale da utilizzare per la fattura
   * **Tipo fattura**: Tipo di documento fattura
   * **Data fattura**: Data della fattura
4. Cliccare su **Crea fatture**

**Stampa selezionati**

Permette di generare una stampa delle rate selezionate:

1. Selezionare le rate da stampare
2. Cliccare su **Stampa selezionati**
3. Verrà generato un PDF con le informazioni delle rate selezionate

***

### Plugin Ricorrenza fatturazione

Il plugin **Ricorrenza fatturazione** è accessibile dalla scheda del contratto e permette di configurare la pianificazione della fatturazione.

<figure><img src="../.gitbook/assets/immagine (1173).png" alt=""><figcaption></figcaption></figure>

Da qui sarà possibile definire la ricorrenza di fatturazione, la data di inizio e l'importo che dovrà avere ogni rata. Al salvataggio delle impostazioni verrà visualizzata una tabella con tutte le scadenze generate:

<figure><img src="../.gitbook/assets/immagine (1175).png" alt=""><figcaption></figcaption></figure>

Sarà ora possibile visualizzare le rate da fatturare dal modulo **Fatturazione contratti,** filtrate in base al mese in corso.

<figure><img src="../.gitbook/assets/immagine (1176).png" alt=""><figcaption></figcaption></figure>

Volendo fatturare le rate manualmente, sarà sufficiente selezionare le rate interessate e cliccare su Crea fattura. Da qui sarà possibile selezionare se accodare le rate selezionate a fatture della stessa anagrafica in stato Bozza, e modificare la data, il sezionale e il tipo di fattura.

<figure><img src="../.gitbook/assets/immagine (1177).png" alt=""><figcaption></figcaption></figure>

Cliccando su Crea fatture si procede alla fatturazione delle rate selezionate:

<figure><img src="../.gitbook/assets/immagine (1178).png" alt=""><figcaption></figcaption></figure>

Tornando al contratto e navigando al plugin Ricorrenza fatturazione è ora possibile visualizzare la rata appena fatturata.

<figure><img src="../.gitbook/assets/immagine (1179).png" alt=""><figcaption></figcaption></figure>

#### Accesso al plugin

1. Navigare in **Contratti**
2. Selezionare un contratto esistente o crearne uno nuovo
3. Cliccare sulla scheda **Ricorrenza fatturazione**

#### Configurazione della ricorrenza

**Campi disponibili**

| Campo                    | Descrizione                                                     | Obbligatorio |
| ------------------------ | --------------------------------------------------------------- | ------------ |
| Ricorrenza fatturazione  | Selezionare la cadenza (Mensile, Bimestrale, Trimestrale, ecc.) | Sì           |
| Cadenza                  | Scegliere tra Anticipata o Posticipata                          | Sì           |
| Data inizio fatturazione | Data da cui far partire la prima fattura                        | Sì           |
| Importo fatturazione     | Importo totale che verrà applicato a ogni rata                  | Sì           |

**Cadenza anticipata vs posticipata**

**Anticipata**:

* La rata viene generata all'inizio del periodo di fatturazione
* Esempio: 01/01 per il periodo Gennaio-Marzo

**Posticipata**:

* La rata viene generata alla fine del periodo di fatturazione
* Esempio: 31/03 per il periodo Gennaio-Marzo

#### Visualizzazione delle scadenze

Dopo aver salvato la configurazione, viene visualizzata una tabella con tutte le scadenze generate:

| Colonna   | Descrizione                                                               |
| --------- | ------------------------------------------------------------------------- |
| Scadenza  | Data della scadenza della rata                                            |
| Rata      | Numero progressivo della rata                                             |
| Documento | Link alla fattura (se già fatturata) o indicazione "Non ancora fatturato" |
| Importo   | Importo della rata                                                        |

#### Requisiti del contratto

Per poter configurare la ricorrenza fatturazione, il contratto deve soddisfare i seguenti requisiti:

* **Data di accettazione**: Deve essere impostata (diversa da 0000-00-00)
* **Data di conclusione**: Deve essere impostata (diversa da 0000-00-00)
* **Stato**: Deve essere in uno stato fatturabile (es. "In lavorazione")

***

### Fatturazione manuale

#### Creazione di fatture per le rate

Per fatturare manualmente le rate:

1. Accedere al modulo **Fatturazione contratti**
2. Utilizzare i filtri per visualizzare le rate desiderate
3. Selezionare le rate da fatturare
4. Cliccare su **Crea fattura**
5. Configurare i parametri della fattura:
   * **Accodare**: Se attivo, le rate vengono accodate a fatture esistenti in stato Bozza
   * **Sezionale**: Sezionale da utilizzare
   * **Tipo fattura**: Tipo di documento (es. Fattura immediata di vendita)
   * **Data fattura**: Data della fattura
6. Cliccare su **Crea fatture**

#### Gestione delle fatture create

Le fatture create vengono automaticamente associate al modulo **Fatture di vendita** e possono essere gestite da lì.

#### Stato delle fatture

Lo stato delle fatture create dipende dall'impostazione **Cron fatturazione**:

* Se impostato su `Crea in bozza`: Le fatture vengono create in stato **Bozza**
* Altrimenti: Le fatture vengono create in stato **Emessa**

#### Generazione della fattura elettronica

Se l'impostazione **Cron fatturazione** include l'opzione **Emetti**, viene automaticamente generata la fattura elettronica XML.

#### Invio della copia di cortesia

Se l'impostazione **Cron fatturazione** include l'opzione **PDF**, viene inviata automaticamente una copia di cortesia via email al cliente.

#### Invio allo SDI

Se l'impostazione **Cron fatturazione** include l'opzione **XML**, l'XML viene inviato allo SDI dopo il numero di giorni specificato nell'impostazione **Elaborazione invio automatico XML**.

***

### Automatizzazione con Cron

#### Configurazione dello script cron

Per automatizzare la fatturazione, è necessario configurare un job cron che esegua lo script `cron/fatturazione_contratti.php`.

**Esempio di configurazione**

```bash
# Esegui ogni giorno alle 02:00
0 2 * * * php /percorso/dello/stamanager/cron/fatturazione_contratti.php
```

**Esempio con log**

```bash
# Esegui ogni giorno alle 02:00 con salvataggio del log
0 2 * * * php /percorso/dello/stamanager/cron/fatturazione_contratti.php >> /var/log/fatturazione_contratti.log 2>&1
```

### Differenze con il plugin Pianifica fatturazione

Il modulo **Fatturazione programmata contratti** differisce dal plugin **Pianifica fatturazione** in diversi aspetti fondamentali:

#### Suddivisione delle righe

| Caratteristica     | Pianifica fatturazione                                          | Fatturazione programmata contratti                    |
| ------------------ | --------------------------------------------------------------- | ----------------------------------------------------- |
| Suddivisione righe | Richiede che le righe del contratto siano già suddivise in rate | Non richiede suddivisione predefinita delle righe     |
| Flessibilità       | Limitata alla struttura delle righe esistenti                   | Completamente flessibile nella definizione delle rate |

#### Impostazione della ricorrenza

| Caratteristica | Pianifica fatturazione                 | Fatturazione programmata contratti                    |
| -------------- | -------------------------------------- | ----------------------------------------------------- |
| Ricorrenza     | Fissa in base alle righe del contratto | Configurabile liberamente (Mensile, Bimestrale, ecc.) |
| Data inizio    | Derivata dalle righe del contratto     | Configurabile liberamente                             |
| Importo rata   | Derivato dalle righe del contratto     | Configurabile liberamente                             |

#### Vista delle scadenze

| Caratteristica       | Pianifica fatturazione | Fatturazione programmata contratti             |
| -------------------- | ---------------------- | ---------------------------------------------- |
| Visualizzazione      | Per singolo contratto  | Vista generica suddivisa per mese              |
| Filtri               | Limitati               | Avanzati (cliente, contratto, data, pagamento) |
| Fatturazione massiva | Non supportata         | Supportata con azione di gruppo                |

#### Automazione

| Caratteristica         | Pianifica fatturazione | Fatturazione programmata contratti    |
| ---------------------- | ---------------------- | ------------------------------------- |
| Script cron            | Non disponibile        | Configurabile con diverse opzioni     |
| Invio automatico XML   | Non disponibile        | Configurabile con ritardo programmato |
| Invio automatico email | Non disponibile        | Configurabile                         |

#### Cadenza delle rate

| Caratteristica         | Pianifica fatturazione | Fatturazione programmata contratti   |
| ---------------------- | ---------------------- | ------------------------------------ |
| Anticipata/Posticipata | Non supportata         | Supportata con campo `is_anticipato` |

#### Riepilogo

Il modulo **Fatturazione programmata contratti** offre:

* Maggiore flessibilità nella configurazione delle rate
* Vista centralizzata di tutte le scadenze
* Automazione completa della fatturazione
* Gestione avanzata della cadenza delle rate
* Filtri e ricerca avanzati

Il plugin **Pianifica fatturazione** è più adatto per:

* Contratti con struttura rigida e predefinita
* Scenari dove la suddivisione delle rate è già definita nelle righe del contratto
* Utilizzo senza necessità di automazione

***

## Changelog

Tutti i maggiori cambiamenti di questo progetto saranno documentati in questo file. Per informazioni più dettagliate, consultare il log GIT della repository su GitHub.

Il formato utilizzato è basato sulle linee guida di [Keep a Changelog](http://keepachangelog.com/), e il progetto segue il [Semantic Versioning](http://semver.org/) per definire le versioni delle release.

* 7.0 (2026-03-19)
* 6.0 (2026-02-02)
* 5.2 (2025-11-18)
* 5.1 (2025-06-30)
* 5.0 (2025-03-21)
* 4.2 (2024-11-22)
* 4.1 (2024-08-01)
* 4.0 (2024-06-04)
* 3.2 (2024-04-03)
* 3.1 (2024-02-19)
* 3.0 (2023-12-01)
* 2.1 (2023-11-29)
* 2.0 (2023-10-25)
* 1.0 (2023-06-07)

### 7.0(2026-03-19)

#### Aggiunto (Added)

* Aggiunta l'automazione del rilascio tramite `gulpfile.js` e `package.json`
* Aggiunta la generazione dei file JSON di struttura e configurazione per i controlli di integrità

#### Modificato (Changed)

* Aggiornata la toolchain di sviluppo con compatibilità Node.js moderna, Yarn 4 e Rector 2
* Aggiornata la compatibilità del modulo alla serie `2.10.*`

#### Fixed

* Corretta la gestione delle date in cron, AJAX contratti e visualizzazione ricorrenze per evitare errori di conversione

### 6.0(2026-02-02)

#### Aggiunto (Added)

* Introdotto il campo `is_anticipato` per la generazione delle rate con cadenza anticipata e posticipata

### 5.2(2025-11-18)

#### Aggiunto (Added)

* Aggiunta l'impostazione per generare fatture in bozza
* Aggiunto l'ordinamento dei contratti per ragione sociale

#### Fixed

* Correzioni minori nella fatturazione

### 5.1(2025-06-30)

#### Aggiunto (Added)

* Aggiunto il controllo sulla presenza delle rate prima della generazione

#### Fixed

* Corretta la gestione del cron di fatturazione contratti

### 5.0(2025-03-21)

#### Modificato (Changed)

* Allineato il modulo alla versione `2.7.1`

#### Fixed

* Corretta la gestione AJAX dei contratti
* Corretta la visualizzazione del grafico del modulo

### 4.2(2024-11-22)

#### Fixed

* Aggiunta la classe mancante necessaria al corretto funzionamento del modulo

### 4.1(2024-08-01)

#### Fixed

* Correzioni minori sulla fatturazione del modulo

### 4.0(2024-06-04)

#### Aggiunto (Added)

* Aggiunto rector
* Adattamento versione 2.5.2

### 3.2(2024-04-03)

#### Aggiunto (Added)

* Aggiunta la ricerca nel modulo

#### Fixed

* Corretto il link alla fattura

### 3.1(2024-02-19)

#### Aggiunto (Added)

* Aggiunta la stampa contratti selezionati
* Aggiunto ordinamento per rata e data rata in fatturazione contratti
* Aggiunto php-cs-fix

#### Fixed

* Corretta la visualizzazione delle rate fatturate dal plugin

### 3.0(2023-12-01)

#### Aggiunto (Added)

* Aggiunto file custom/variables.php per risalire alle variabili del contratto
* Aggiunta colonna rata a elenco rate da Ricorrenza fatturazione

#### Modificato (Changed)

* Modificata la visualizzazione rate includendo tutte le rate e togliendo il filtro per periodo

#### Fixed

* Corretta la visualizzazione delle rate in Ricorrenza fatturazione
* Corretta la funzione di accodamento a documenti esistenti
* Corretta l'emissione della fattura generata per includere le righe del documento

### 2.1(2023-11-29)

#### Aggiunto (Added)

* Aggiunta la tabella per visualizzare le rate già fatturate in Ricorrenza fatturazione

### 2.0(2023-10-25)

#### Aggiunto (Added)

* Aggiunto lo script da impostare in cron per la generazione automatica delle fatture, invio delle fatture elettroniche allo SDI e invio della copia di cortesia della fattura al cliente via mail

#### Modificato (Changed)

* Migliorata la grafica dei filtri del modulo

### 1.0(2023-06-07)

#### Fixed

* Correzioni minori sul file di aggiornamento iniziale `1_0.sql`

***

### Supporto

Per assistenza tecnica o segnalazione di bug, consultare la documentazione ufficiale di OpenSTAManager o contattare il supporto tecnico.

### Licenza

Questo modulo è distribuito sotto licenza GNU General Public License versione 3 o successiva.

***

**Ultimo aggiornamento**: 19 Marzo 2026\
**Versione documentazione**: 1.0\
**Versione modulo**: 7.0
