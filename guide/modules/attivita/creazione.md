---
title: Creazione attività
---

# Creazione

La creazione di nuovi elementi segue il funzionamento standard del gestionale, necessitando il click sul pulsante apposito all'interno dell'intestazione del modulo.

![Screenshot creazione attivit&#xE0;](../../../.gitbook/assets/add-attivita.PNG)

Il modulo **Attività** presenta quindi la possibilità di inserire le informazioni complete relative alla nuova attività da creare.

## Caratteristiche

Il sistema di creazione di un nuovo elemento permette il completamento delle informazioni di base fondamentali per il processo di inizializzazione dell'attività. Queste vengono divise in tre sezioni principali:

* Dati cliente
* Dati intervento
* Ore di lavoro

![Screenshot creazione attivit&#xE0;](../../../.gitbook/assets/sezioniattivita.PNG)

### Dati cliente

La sezione _Dati cliente_ si occupa della gestione dei dati dell'attività interagenti con altri moduli:

* Cliente dell'attività
* Sede di esecuzione attività
* Cliente per conto di cui viene eseguita l'attività
* Zona\(definita automaticamente in base al cliente selezionato\)
* Preventivo collegato
* Contratto collegato
* Impianto dell'attività
* Componenti dell'impianto interessati

![Screenshot dati cliente](../../../.gitbook/assets/screendaticlienti.PNG)

### Dati intervento 

Parallelamente, la componente _Dati intervento_ permette la compilazione di alcune informazioni generali, quali:

* Data e ora richiesta
* Tipo di attività
* Stato dell'attività da creare
* Richiesta

![Screenshot dati intervento](../../../.gitbook/assets/screendatiintervento.PNG)

### Ore di lavoro

La sezione _Ore di lavoro_ si occupa di determinare durata dell'attività e il tecnico assegnato, composto dai seguenti campi:

* Inizio attività
* Fine attività
* Tecnici

![Screenshot ore di lavoro](../../../.gitbook/assets/screenoredilavoro.PNG)

\#

### Creazione anagrafica al volo

Nella schermata di creazione di una nuova attività viene permessa la creazione al volo dell'anagrafica di tipo _Cliente_ relativa al nuovo _record_. Questa funzionalità viene permessa dal pulsante dedicato a destra del selettore del campo _Cliente_.

![Screenshot creazione anagrafica al volo](../../../.gitbook/assets/creazionealvolocliente.PNG)

La gestione della creazione viene quindi delegata al modulo **Anagrafiche**, permettendo l'inserimento delle informazioni standard documentate nella [sezione relativa](../anagrafiche/creazione.md) attraverso un _modal_ sovrapposto al resto del contenuto.

![Screenshot creazione anagrafica al volo](../../../.gitbook/assets/creazionealvolocliente2.PNG)

Una volta completata la creazione in questione, l'anagrafica creata verrà automaticamente selezionata.

## Particolarità

Creare un'attività senza tecnici selezionati la aggiungerà al widget **Promemoria attività da pianificare** della **Dashboard**.

![Widget promemoria attivit&#xE0; da pianificare presente nella Dashboard](../../../.gitbook/assets/promemoriaattivitadapianificare.PNG)

