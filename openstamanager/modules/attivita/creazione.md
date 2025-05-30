---
description: Come creare un'attività in OpenSTAManager
---

# ➕ Creazione

er creare un'attività in OpenSTAManager si dovrà cliccare sul tasto (+).

La schermata che si presenterà sarà questa, dove sarà possibile inserire:

* [Cliente](creazione.md#anagrafica)
* [Sede destinazione](creazione.md#sede-destinazione)
* Per conto di
* [Impianto](creazione.md#impianto)
* Componenti
* Sezionale
* Preventivo
* [Contratto](creazione.md#contratto)
* Ordine
* Data/ora richiesta
* Tipo
* Stato
* Richiesta
* Descrizione

<figure><img src="../../../.gitbook/assets/immagine (1075).png" alt=""><figcaption></figcaption></figure>

Si possono notare anche diverse sottosezioni:

* [Dettagli cliente](creazione.md#dettagli-cliente)
* [Posizione](creazione.md#posizione)
* [Dettagli aggiuntivi](creazione.md#dettagli-aggiuntivi)
* [Assegnazione tecnici](creazione.md#assegnazione-tecnici)
* [Sessioni di lavoro](creazione.md#ore-di-lavoro)
* [Ricorrenza](creazione.md#ricorrenza)

### 🗺️ Posizione

Viene qui localizzato il cliente sulla mappa

### ✒️ Dettagli aggiuntivi

In questa sezione sarà possibile inserire:

* Data/ora scadenza
* Referente

### 🧑‍🔧 Assegnazione tecnici

La sezione _Assegnazione tecnici_ si occupa della gestione dei tecnici dell'attività:

* [Tecnici assegnati](creazione.md#tecnico)

### ⏰ Sessioni di lavoro

Da questa sezione è possibile determinare la durata dell'attività e il tecnico assegnato, nei seguenti campi:

* Inizio attività
* Fine attività
* Zona
* Tecnici (con possibilità di [crearlo al momento](creazione.md#creazione-impianto-al-volo))

### 🔁 Ricorrenza

Nella sezione Ricorrenza è possibile dichiarare se l'attività è ricorrente o meno

### 🧿 Dettagli cliente

Nella sezione Dettagli cliente vengono visualizzati i Contratti, Preventivi e Fatture attivi per il cliente selezionato, e vengono visualizzate le note interne.

## 💸 Creazione di Record al volo

Cliccando sul tasto (+) alla destra del campo di cui dobbiamo inserire un nuovo record, si aprirà una schermata in cui sarà possibile inserire i valori del nuovo record che si andrà a creare.

### 👤 Anagrafica

L'unico campo obbligatorio per creare un'anagrafica al volo è Denominazione, si potrà procedere in un secondo momento a [completare](../anagrafiche/modifica.md) gli altri campi entrando nel nuovo record in anagrafica.

<figure><img src="../../../.gitbook/assets/immagine (1076).png" alt=""><figcaption></figcaption></figure>

### 🏭 Sede destinazione

I campi obbligatori per creare una sede al volo sono Nome sede e città, si potrà procedere in un secondo momento a [completare](../anagrafiche/plugin/sedi.md) gli altri campi entrando nel nuovo record tra le sedi del cliente scelto.

<figure><img src="../../../.gitbook/assets/immagine (1077).png" alt=""><figcaption></figcaption></figure>

### 📄 Contratto

I campi obbligatorio per creare un contratto al volo sono Nome e Stato, si potrà procedere in un secondo momento a [completare](https://github.com/devcode-it/openstamanager-docs/blob/master/modules/attivita/broken-reference/README.md) gli altri campi entrando nel nuovo record in Vendite/Contratti.

<figure><img src="../../../.gitbook/assets/immagine (1078).png" alt=""><figcaption></figcaption></figure>

### 🧑 Referente

I campi obbligatorio per creare un contratto al volo sono Nominativo, Mansione e Sede, si potrà procedere in un secondo momento a [completare](https://docs.openstamanager.com/modules/anagrafiche/plugin/referenti#modifica) gli altri campi entrando nel nuovo record tra i referenti del cliente scelto.

<figure><img src="../../../.gitbook/assets/immagine (1079).png" alt=""><figcaption></figcaption></figure>

### 📡 Impianto

I campi obbligatorio per creare un contratto al volo sono Matricola e Nome, si potrà procedere in un secondo momento a [completare](../impianti/modifica.md) gli altri campi entrando nel nuovo record tra gli impianti.

<figure><img src="../../../.gitbook/assets/immagine (1080).png" alt=""><figcaption></figcaption></figure>

### 🧑‍🔧 Tecnico

L'unico campo obbligatorio per creare un'anagrafica di tipo tecnico al volo è Denominazione, si potrà procedere in un secondo momento a [completare](../anagrafiche/modifica.md) gli altri campi entrando nel nuovo record in anagrafica.

<figure><img src="../../../.gitbook/assets/immagine (1081).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Creare un'attività senza tecnici selezionati la aggiungerà al widget **Promemoria attività da pianificare** della **Dashboard**.
{% endhint %}

![Widget promemoria attività da pianificare presente nella Dashboard](../../../.gitbook/assets/PromemoriaAttivitàDaPianificare.PNG)
