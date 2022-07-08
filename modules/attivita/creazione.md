---
title: Creazione attività
description: Come creare un'attività in OpenSTAManager
---

# ➕ Creazione

Per creare un'attività in OpenSTAManager si dovrà cliccare sul tasto (+).

La schermata che si presenterà sarà questa, dove sarà possibile inserire:

* Cliente (con possibilità di [crearlo al momento](creazione.md#creazione-impianto-al-volo))
* Sede destinazione (con possibilità di [crearla al momento](creazione.md#creazione-impianto-al-volo))
* Per conto di
* Preventivo
* Contratto (con possibilità di [crearlo al momento](creazione.md#creazione-impianto-al-volo))
* Ordine
* Referente (con possibilità di [crearlo al momento](creazione.md#creazione-impianto-al-volo))
* Tipo
* Stato
* Richiesta

![](<../../.gitbook/assets/Senzanome (1).png>)

Si possono notare anche 5 sottosezioni:

* [Dettagli aggiuntivi](creazione.md#dettagli-aggiuntivi)
* [Assegnazione tecnici](creazione.md#assegnazione-tecnici)
* [Ore lavoro](creazione.md#ore-di-lavoro)
* [Ricorrenza](creazione.md#ricorrenza)
* [Dettagli cliente](creazione.md#dettagli-cliente)

### ✒️ Dettagli aggiuntivi

In questa sezione sarà possibile inserire:

* Data/ora scadenza
* Impianto (con possibilità di [crearlo al momento](creazione.md#creazione-impianto-al-volo))
* Componenti

![](<../../.gitbook/assets/image (83) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

### 🧑‍🔧 Assegnazione tecnici

La sezione _Assegnazione tecnici_ si occupa della gestione dei tecnici dell'attività:

* Tecnici assegnati (con possibilità di [crearlo al momento](creazione.md#creazione-impianto-al-volo))

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FVylZtPBDizmjzIvAB1h7%2Ffile.png?alt=media)

### ⏰ Ore di lavoro

La sezione _Ore di lavoro_ si occupa di determinare durata dell'attività e il tecnico assegnato, composto dai seguenti campi:

* Inizio attività
* Fine attività
* Zona
* Tecnici (con possibilità di [crearlo al momento](creazione.md#creazione-impianto-al-volo))

![](<../../.gitbook/assets/image (75) (1) (1) (1) (1) (1) (1).png>)

### 🔁 Ricorrenza

Nella sezione Ricorrenza è possibile dichiarare se l'attività è ricorrente o meno:

![](<../../.gitbook/assets/image (60) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

### 🧿 Dettagli cliente

Nella sezione Dettagli cliente vengono visualizzati i Contratti, Preventivi e Fatture attivi per il cliente selezionato, e vengono visualizzate le note interne.

![](<../../.gitbook/assets/image (70) (1) (1) (1) (1) (1).png>)

## 💸 Creazione di Record al volo

Cliccando sul tasto (+) alla destra del campo di cui dobbiamo inserire un nuovo record, si aprirà una schermata in cui sarà possibile inserire i valori del nuovo record che si andrà a creare.

### 👤 Anagrafica

L'unico campo obbligatorio per creare un'anagrafica al volo è Denominazione, si potrà procedere in un secondo momento a [completare](../anagrafiche/modifica.md) gli altri campi entrando nel nuovo record in anagrafica.

![](<../../.gitbook/assets/image (99) (1) (1).png>)

### 🏭 Sede destinazione

I campi obbligatori per creare una sede al volo sono Nome sede e città, si potrà procedere in un secondo momento a [completare](../anagrafiche/plugin/sedi.md) gli altri campi entrando nel nuovo record tra le sedi del cliente scelto.

![](<../../.gitbook/assets/image (27) (1) (1) (1).png>)

### 📄 Contratto

I campi obbligatorio per creare un contratto al volo sono Nome e Stato, si potrà procedere in un secondo momento a [completare](broken-reference/) gli altri campi entrando nel nuovo record in Vendite/Contratti.

![](<../../.gitbook/assets/image (31) (1) (1) (1) (1) (1) (2) (1).png>)

### 🧑 Referente

I campi obbligatorio per creare un contratto al volo sono Nominativo, Mansione e Sede, si potrà procedere in un secondo momento a [completare](https://docs.openstamanager.com/modules/anagrafiche/plugin/referenti#modifica) gli altri campi entrando nel nuovo record tra i referenti del cliente scelto.

![](<../../.gitbook/assets/image (57) (1) (1) (1) (1) (1) (1).png>)

### 📡 Impianto

I campi obbligatorio per creare un contratto al volo sono Matricola e Nome, si potrà procedere in un secondo momento a [completare](../impianti/modifica.md) gli altri campi entrando nel nuovo record tra gli impianti.

![](<../../.gitbook/assets/image (58) (1) (1) (1) (1) (1) (1).png>)

### 🧑‍🔧 Tecnico

L'unico campo obbligatorio per creare un'anagrafica di tipo tecnico al volo è Denominazione, si potrà procedere in un secondo momento a [completare](../anagrafiche/modifica.md) gli altri campi entrando nel nuovo record in anagrafica.

![](<../../.gitbook/assets/image (56) (1) (1) (1) (1) (1) (1) (1) (1).png>)

{% hint style="warning" %}
Creare un'attività senza tecnici selezionati la aggiungerà al widget **Promemoria attività da pianificare** della **Dashboard**.
{% endhint %}

![Widget promemoria attività da pianificare presente nella Dashboard](../../.gitbook/assets/PromemoriaAttivitàDaPianificare.PNG)
