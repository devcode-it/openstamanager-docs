---
title: Creazione attività
---

# creazione

La creazione di nuovi elementi segue il funzionamento standard del gestionale, necessitando il click sul pulsante apposito all'interno dell'intestazione del modulo.

Il modulo **Attività** presenta quindi la possibilità di inserire le informazioni complete relative alla nuova attività da creare.

## Caratteristiche

Il sistema di creazione di un nuovo elemento permette il completamento delle informazioni di base fondamentali per il processo di inizializzazione dell'attività. Queste vengono divise in due sezioni principali:

* Dati cliente
* Dati intervento

La sezione _Dati cliente_ si occupa della gestione dei dati dell'attività interagenti con altri moduli:

* Cliente dell'attività
* Sede di esecuzione attività
* Cliente per conto di cui viene eseguita l'attività
* Referente di contatto
* Preventivo collegato
* Contratto collegato
* Impianto dell'attività
* Componenti dell'impianto interessati

Parallelamente, la componente _Dati intervento_ permette la compilazione di alcune informazioni generali, quali:

* Data di richiesta
* Zona
* Tipo di attività
* Stato dell'attività da creare
* Tecnici coinvolti
* Richiesta

In base alla selezione dei tecnici, i campi _Data attività_, _Orario inizio_ e _Orario fine_ creeranno altrettante sessioni di lavoro dopo aver completato l'inizializzazione della nuova attività.

### Creazione anagrafica al volo

Nella schermata di creazione di una nuova attività viene permessa la creazione al volo dell'anagrafica di tipo _Cliente_ relativa al nuovo _record_. Questa funzionalità viene permessa dal pulsante dedicato a destra del selettore del campo _Cliente_.

La gestione della creazione viene quindi delegata al modulo **Anagrafiche**, permettendo l'inserimento delle informazioni standard documentate nella [sezione relativa](../anagrafiche/creazione.md) attraverso un _modal_ sovrapposto al resto del contenuto.

Una volta completata la creazione in questione, l'anagrafica creata verrà automaticamente selezionata.

## Particolarità

Creare un'attività senza tecnici selezionati la aggiungerà al widget **Promemoria attività da pianificare** della **Dashboard**.

