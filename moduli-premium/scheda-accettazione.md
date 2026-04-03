---
description: Guida al modulo aggiuntivo Scheda accettazione di OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/WzoKFijlVGKTMgti0acZ/moduli-premium/scheda-accettazione
---

# 📗 Scheda accettazione

Scheda accettazione è un modulo che permette la generazione di una scheda di accettazione, un documento pensato per gestire le assistenze tecniche e volto a tutelare entrambe le parti. Su questa scheda infatti vengono riportate le condizioni di assistenza disposte dal negozio, e la richiesta di intervento da parte del cliente.

{% hint style="info" %}
[Clicca qui](https://shop.openstamanager.com/prodotto/scheda-accettazione/) per procedere all'acquisto.
{% endhint %}

### Caratteristiche Principali

Il modulo Scheda Accettazione offre numerose funzionalità per ottimizzare la gestione delle assistenze tecniche:

* ✅ **Creazione rapida anagrafiche**: Possibilità di creare nuove anagrafiche clienti al volo durante l'accettazione
* ✅ **Gestione completa dati cliente**: Raccolta di tutte le informazioni anagrafiche e di contatto
* ✅ **Dettagliati informazioni prodotto**: Registrazione di modello, seriale, dati presenti nel sistema e password
* ✅ **Descrizione problema**: Spazio dedicato per la descrizione del problema a cura del cliente
* ✅ **Gestione tecnici**: Assegnazione di uno o più tecnici all'intervento
* ✅ **Firma digitale**: Supporto per firma tramite tavoletta grafica Wacom
* ✅ **Generazione documenti**: Stampa scheda accettazione completa, semplificata ed etichetta
* ✅ **Invio email**: Possibilità di inviare la scheda accettazione via email al cliente
* ✅ **Condizioni personalizzabili**: Configurazione delle condizioni di assistenza tramite editor
* ✅ **Collegamento contratti**: Collegamento automatico al contratto predefinito del cliente
* ✅ **Gestione sedi**: Supporto per sedi multiple del cliente
* ✅ **Campi compatibili dinamici**: Gestione flessibile dei campi del modulo

***

### Configurazione

#### Impostazioni Generali

Il modulo offre diverse opzioni di configurazione accessibili dal pannello impostazioni di OpenSTAManager:

**Condizioni di Accettazione**

Le condizioni di assistenza tecnica possono essere personalizzate tramite l'editor CKEditor. Le condizioni predefinite includono:

1. Il laboratorio non risponde dell'insorgere di ulteriori guasti non segnalati in sede di accettazione prodotto nonchè dell'accidentale perdita di dati da memoria di massa che si potrebbe verificare durante le fasi di recupero e di intervento intraprese.
2. Saranno riparati esclusivamente i guasti dichiarati dal cliente in fase di accettazione. In caso di guasti non dichiarati, la riparazione verrà effettuata solo previa autorizzazione del cliente.
3. Si consiglia di eseguire un backup dati prima di consegnare il pc al nostro laboratorio. Diversamente sarà possibile usufruire di un servizio di backup a pagamento.
4. La garanzia sugli interventi svolti è valida solo sui componenti hardware.
5. Il ritiro del materiale avverrà previa conferma del supporto tecnico.
6. Il cliente è tenuto a verificare che al momento del ritiro vi sia tutto il materiale consegnato in accettazione. Non saranno accettati reclami successivi all'atto della riconsegna.
7. Saranno applicate le spese di diagnosi fino a un massimo di € 40.00 + IVA nei casi in cui il cliente non accetterà il preventivo di riparazione proposto. Lo stesso importo verrà addebitato nel caso in cui il cliente decida di ritirare l'apparato durante la fase di diagnosi interrompendone la normale lavorazione.
8. Gli apparati non ritirati entro 180gg dalla data di riconsegna comunicata verranno disassemblati e successivamente smaltiti a norma di legge.
9. I pc non ritirati entro 10 giorni lavorativi dal giorno di comunicazione di fine lavori saranno soggetti all'addebito delle spese di giacenza pari a € 3,00 al giorno oltre IVA.

**Sistema di Firma**

Il modulo supporta diverse modalità di firma:

* **Firma standard**: Firma digitale base
* **Tavoletta Wacom**: Supporto per tavoletta grafica con opzioni di luminosità e contrasto personalizzabili

Per configurare la tavoletta Wacom, accedere alle impostazioni e regolare:

* **Luminosità firma Wacom**: Regola la luminosità della firma acquisita
* **Contrasto firma Wacom**: Regola il contrasto della firma acquisita

#### Personalizzazione Campi

È possibile configurare quali campi visualizzare nella schermata di accettazione accedendo alla sezione "Intervento" delle impostazioni. I campi possono essere aggiunti, rimossi o resi obbligatori in base alle esigenze specifiche dell'attività.

***

### Utilizzo del Modulo

#### Creazione di una Nuova Accettazione

Per creare una nuova scheda di accettazione:

1.  **Accesso al modulo**

    Cliccare su "Accettazione" nel menu principale di OpenSTAManager.
2.  **Inserimento dati cliente**

    Compilare i seguenti campi:

    **Dati Anagrafici:**

    * **Tipo attività**: Selezionare il tipo di intervento
    * **Stato**: Definire lo stato dell'intervento
    * **Cliente**: Selezionare un cliente esistente dall'anagrafica OPPURE
    * **Nome e Cognome**: Inserire nome e cognome per creare nuova anagrafica
    * **Ragione sociale**: Per clienti aziendali
    * **Partita IVA**: Numero di partita IVA
    * **Codice fiscale**: Codice fiscale del cliente
    * **Indirizzo**: Indirizzo completo
    * **Città**: Città di residenza/sede
    * **Provincia**: Sigla provincia
    * **CAP**: Codice di avviamento postale
    * **Email**: Indirizzo email per comunicazioni
    * **Telefono**: Numero di telefono fisso
    * **Cellulare**: Numero di cellulare
    * **Sede**: Selezionare la sede (se presente)

<figure><img src="../.gitbook/assets/immagine (6).png" alt=""><figcaption></figcaption></figure>

**Dati Prodotto:**

* **Modello**: Modello del dispositivo in assistenza
* **Seriale**: Numero di serie del prodotto
* **Dati presenti nel sistema**: Informazioni aggiuntive sul dispositivo
* **Password avvio sistema**: Password per l'accesso al sistema
* **Se interessato a teleassistenza**: Flag per servizi di teleassistenza
* **Descrizione del problema**: Descrizione dettagliata del problema a cura del cliente
* **Materiale consegnato**: Elenco degli accessori/consegne
* **Giorni di deposito**: Giorni previsti per il deposito in laboratorio

**Assegnazione Tecnici:**

* **Tecnici**: Selezionare uno o più tecnici da assegnare all'intervento

<figure><img src="../.gitbook/assets/immagine (7).png" alt=""><figcaption></figcaption></figure>

3.  **Creazione attività**

    Cliccare su "Aggiungi firma" per far firmare la scheda di accettazione

<figure><img src="../.gitbook/assets/immagine (8).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/immagine (9).png" alt=""><figcaption></figcaption></figure>

Cliccare su "Crea attività" per procedere con la generazione della scheda di accettazione.

<figure><img src="../.gitbook/assets/immagine (10).png" alt=""><figcaption></figcaption></figure>

#### Gestione Post-Creazione

Dopo aver creato l'attività, il sistema mostrerà un riepilogo con le seguenti opzioni:

**Riepilogo Scheda di accettazione**

Verrà visualizzata una scheda riepilogativa contenente:

* **Numero intervento**: Codice univoco dell'intervento generato
* **Data**: Data della richiesta
* **Cliente**: Link alla scheda anagrafica del cliente
* **Descrizione richiesta**: Testo completo della richiesta del cliente

**Azioni Disponibili**

Dalla schermata di riepilogo è possibile eseguire le seguenti azioni:

1.  **Stampa scheda completa**

    Genera il PDF completo della scheda di accettazione includendo tutte le condizioni di assistenza.
2.  **Stampa senza condizioni**

    Genera una versione semplificata della scheda senza le condizioni di assistenza.
3.  **Stampa etichetta**

    Genera un'etichetta da apporre sul prodotto con i dati essenziali dell'intervento.
4.  **Invia via email**

    Invia la scheda di accettazione al cliente tramite email.
5.  **Vai alla scheda intervento**

    Accede alla scheda completa dell'intervento per gestire eventuali valutazioni o attività di laboratorio.

#### Firma della Scheda

La scheda di accettazione deve essere firmata dal cliente per confermare l'accettazione delle clausole. Il modulo supporta due modalità di firma:

**Firma Standard**

Il cliente può firmare direttamente a video utilizzando mouse o touchpad.

**Firma con Tavoletta Wacom**

Per utilizzi professionali, è possibile utilizzare una tavoletta grafica Wacom per acquisire la firma con maggiore precisione.

**Procedura:**

1. Assicurarsi che la tavoletta sia collegata e riconosciuta dal sistema
2. Selezionare l'opzione "Tavoletta Wacom" nelle impostazioni
3. Il cliente firmerà sulla tavoletta e la firma verrà acquisita automaticamente
4. La firma verrà salvata come immagine JPG nella cartella `/files/accettazione/`

***

### Funzionalità Avanzate

#### Gestione Anagrafiche al Volo

Il modulo permette la creazione di nuove anagrafiche direttamente durante il processo di accettazione, senza dover accedere al modulo Anagrafiche separatamente.

**Funzionamento:**

1. Se non viene selezionato nessun cliente esistente, il sistema crea automaticamente una nuova anagrafica
2. I dati inseriti nel form di accettazione vengono utilizzati per popolare l'anagrafica
3. Il tipo anagrafica viene impostato automaticamente come "Cliente"
4. L'anagrafica viene salvata e collegata all'intervento

#### Collegamento Contratti

Il modulo supporta il collegamento automatico al contratto predefinito del cliente, se presente.

**Requisiti:**

* Il cliente deve avere un contratto impostato come "predefinito"
* Il contratto deve trovarsi in uno stato "pianificabile"
* Il collegamento avviene automaticamente durante la creazione dell'intervento

#### Gestione Sedi

Per clienti con più sedi, è possibile selezionare la sede specifica da cui parte l'intervento.

#### Invio Email Automatico

È possibile configurare l'invio automatico della scheda accettazione via email al cliente. La funzionalità utilizza il sistema di email di OpenSTAManager e permette di:

* Selezionare il template email da utilizzare
* Inviare la scheda come allegato PDF
* Personalizzare il testo del messaggio

#### Campi Compatibili Dinamici

Dalla versione 5.0, il modulo supporta campi compatibili dinamici, permettendo una gestione più flessibile delle informazioni da raccogliere durante l'accettazione.

***

### Templates Disponibili

Il modulo include tre template per la generazione dei documenti:

#### 1. Scheda Accettazione (Completa)

**File:** `templates/scheda_accettazione/`

**Caratteristiche:**

* Include tutte le informazioni dell'intervento
* Contiene le condizioni complete di assistenza
* Include lo spazio per la firma del cliente
* Formattazione professionale e completa

**Utilizzo:** Stampa della scheda completa da far firmare al cliente e conservare agli atti.

#### 2. Scheda Accettazione (Senza Condizioni)

**File:** `templates/scheda_accettazione/` (opzione `condizioni: false`)

**Caratteristiche:**

* Include le informazioni essenziali dell'intervento
* Non contiene le condizioni di assistenza
* Più sintetica e immediata

**Utilizzo:** Stampa per utilizzi interni o quando le condizioni sono già state accettate separatamente.

#### 3. Etichetta Accettazione

**File:** `templates/etichette_accettazione/`

**Caratteristiche:**

* Formato compatto per etichette
* Contiene i dati essenziali: numero intervento, data, cliente
* Nome file dinamico: `Etichetta num. {numero} del {data}`

**Utilizzo:** Etichetta da apporre sul prodotto per identificazione rapida durante le fasi di lavorazione.

***

### Sistema di Firma

#### Configurazione

Il sistema di firma è configurabile dalle impostazioni del modulo. Le opzioni disponibili sono:

**Modalità Firma**

* **Standard**: Firma tramite mouse/touchpad
* **Tavoletta Wacom**: Firma tramite tavoletta grafica professionale

**Impostazioni Tavoletta Wacom**

Per ottimizzare l'acquisizione della firma tramite tavoletta Wacom:

* **Luminosità**: Regola la luminosità dell'immagine della firma (valore float)
* **Contrasto**: Regola il contrasto dell'immagine della firma (valore float)

#### Salvataggio Firma

Le firme vengono salvate come immagini JPEG nella directory:

```
/files/accettazione/firma_{timestamp}.jpg
```

Il nome del file segue il formato `firma_{timestamp}.jpg` per garantire l'univocità.

#### Visualizzazione Firma

La firma salvata viene:

* Associata all'intervento nel database
* Visualizzata nella scheda intervento
* Inclusa nel PDF della scheda accettazione

#### Modalità Tavoletta Wacom

Per utilizzare la tavoletta Wacom:

1. Installare i driver della tavoletta sul sistema
2. Configurare l'impostazione "Sistema di firma" su "Tavoletta Wacom"
3. Regolare luminosità e contrasto se necessario
4. Il cliente firmerà sulla tavoletta durante l'accettazione

**Vantaggi:**

* Maggiore precisione della firma
* Aspetto più professionale
* Migliore leggibilità della firma nel documento

***

## Changelog

### 6.0 (2026-03-10)

#### Aggiunto (Added)

* Aggiunto file JSON per controllo integrità
* Aggiunto gulpfile e package.json per automazione build
* Generazione file .json per controlli integrità

### 5.1 (2025-12-16)

#### Corretto (Fixed)

* Fix installazione
* Fix minore

### 5.0 (2025-07-22)

#### Aggiunto (Added)

* Campi compatibili dinamici

#### Modificato (Changed)

* Miglioria grafica modulo scheda accettazione

#### Corretto (Fixed)

* Fix stampa scheda accettazione

### 4.1 (2025-07-15)

#### Aggiunto (Added)

* Aggiunta test

#### Corretto (Fixed)

* Fix query installazione

### 4.0 (2025-02-14)

#### Aggiunto (Added)

* Collegamento contratto predefinito del cliente

#### Corretto (Fixed)

* Fix stile pulsante crea attività
* Fix creazione cliente al volo in scheda accettazione

### 3.2 (2024-10-11)

#### Corretto (Fixed)

* Fix modulo scheda accettazione

### 3.1 (2024-08-08)

#### Aggiunto (Added)

* Gestione firma accettazione con tavoletta Wacom

### 3.0 (2024-06-14)

#### Aggiunto (Added)

* Aggiunto rector
* Allineamento a OSM 2.5.2

#### Corretto (Fixed)

* Fix modulo

### 2.2 (2024-02-19)

#### Aggiunto (Added)

* Aggiunta campo sede

#### Corretto (Fixed)

* Fix invio via mail
* Fix minore

### 2.1 (2024-01-26)

#### Aggiunto (Added)

* Aggiunto invio mail scheda accettazione
* Aggiunto php-cs-fixer
* Aggiunta firma da tavoletta grafica in base all'impostazione "Sistema di firma"

#### Corretto (Fixed)

* Fix

### 2.0 (2023-07-18)

#### Corretto (Fixed)

* Fix condizioni accettazioni
* Fix scheda accettazione
* Fix stampa scheda accettazione

### 1.0 (2022-12-07)

#### Aggiunto (Added)

* Migliorie per installazione automatica
* Creati modelli per inserimento campi
* Aggiunta file MODULE
* Aggiunta condizioni prima di firmare
* Check valori required
* Aggiunta condizioni da impostazioni

#### Corretto (Fixed)

* Fix compilazione campi
* Fix creazione nuova anagrafica al volo
* Fix codice intervento in stampa accettazione
* Allineamento 2.4.20

***

#### Vai alla videoguida:

{% content-ref url="../guide/videoguide/scheda-accettazione.md" %}
[scheda-accettazione.md](../guide/videoguide/scheda-accettazione.md)
{% endcontent-ref %}
