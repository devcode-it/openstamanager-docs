---
description: Guida alle azioni aggiuntive del modulo Attività di OpenSTAManager
---

# ❗ Azioni aggiuntive

## 👥 Dal modulo Attività

Il modulo Attività presenta le seguenti funzioni:

* Vedere le attività create direttamente a calendario dal modulo [Dashboard](../dashboard/);
* Selezionare dalla checkbox a inizio riga le attività interessate e cliccando su Azioni di gruppo
  * Esportarne le stampe
  * Fatturarle massivamente
  * Cambiare loro massivamente lo stato
  * Duplicarle
  * Stamparne il riepilogo
* [Sincronizzare](../../esempi/calendario-su-telefono.md) gli interventi dei tecnici con calendari esterni attraverso il sistema API ufficiale.

### 📅 Vedere le attività da Dashboard

Nella Dashboard è possibile visualizzare eventi creati dal modulo Attività, per avere un maggior controllo degli interventi con la vista a calendario.

Le [attività create da calendario](../dashboard/creazione.md) si riscontreranno poi nell'elenco delle attività e sarà possibile modificarle da qui, cliccando sul rispettivo record.

![](<../../.gitbook/assets/image (34) (1) (1) (1) (1) (1) (1) (2) (1).png>)

### 📤 Esportazione stampe

Una volta selezionati i record interessati è possibile esportare massivamente le stampe cliccando su Azioni di gruppo/Esporta stampe.

![](<../../.gitbook/assets/image (63) (1) (1) (1) (1) (1) (1) (1) (1).png>)

Il gestionale chiederà quindi la conferma di procedere all'esportazione in formato ZIP delle stampe delle attività selezionate.

![](<../../.gitbook/assets/image (99) (1).png>)

Cliccando su procedi si confermerà l'operazione.

### 📃 Fatturazione massiva

Una volta selezionati i record interessati è possibile fatturare massivamente le attività cliccando su Azioni di gruppo/Fattura interventi.

![](<../../.gitbook/assets/image (54) (1) (1) (1) (1) (1).png>)

Il gestionale chiederà quindi la conferma a procedere alla fatturazione, permettendo di scegliere:

* Se aggiungere le righe degli interventi selezionati a una fattura di vendita in bozze dello stesso cliente
* il sezionale in cui andare a registrare le fatture di vendita
* il tipo di documento che si andrà a creare

Cliccando su procedi si confermerà la fatturazione.

![](<../../.gitbook/assets/image (64) (1) (1) (2).png>)

Sarà ora possibile visualizzare la fattura di vendita appena creata nel modulo Vendite/Fatture di vendita, e analizzandola nel dettaglio si troveranno tra le righe le specifiche dei tre interventi svolti.

![](<../../.gitbook/assets/image (55) (1) (1) (2) (1) (1) (1) (1).png>)

![](<../../.gitbook/assets/image (62) (1) (1) (1).png>)

### ⚙️ Modifica dello stato massivo

Una volta selezionati i record interessati è possibile modificarne lo stato massivamente cliccando su Azioni di gruppo/Cambia stato.

![](<../../.gitbook/assets/image (103) (1) (1) (1) (1).png>)

Il gestionale chiederà quindi la conferma a procedere alla modifica dello stato, permettendo di scegliere tra gli stati presenti:

* Completato
* Da programmare
* Fatturato
* Programmato
* (eventuali stati personalizzati)

![](<../../.gitbook/assets/image (24) (1) (1) (1) (1) (1) (1).png>)

Cliccando su Procedi si confermerà l'operazione.

### 🧬 Duplicazione massiva

Una volta selezionati i record interessati è possibile duplicarli massivamente cliccando su Azioni di gruppo/Duplica attività.

![](<../../.gitbook/assets/image (98) (1) (1) (1) (1).png>)

Il gestionale chiederà quindi la conferma a procedere alla duplicazione dei record, permettendo di scegliere:

* La data e ora della richiesta
* Lo [stato](statidiattivita.md) in cui impostare i record che verranno creati
* Se duplicare anche le righe dei record selezionati
* Se duplicare anche le sessioni dei record selezionati

Cliccando su Procedi il gestionale procederà alla duplicazione.

![](<../../.gitbook/assets/image (80) (1) (1) (1) (1) (1).png>)

Si potranno ora vedere tra le attività i record appena creati.

![](<../../.gitbook/assets/image (66) (1) (1) (1) (1) (1) (1).png>)

### 🖨️ Stampa massiva

Una volta selezionati i record interessati è possibile stamparli massivamente cliccando su Azioni di gruppo/Stampa riepilogo.

![](<../../.gitbook/assets/image (52) (1) (2).png>)

Il gestionale chiederà quindi la conferma a procedere alla stampa dei record, permettendo di scegliere tra:

* Riepilogo clienti (con costi addebitati al cliente)
* Riepilogo interno (con costi interni del tecnico)

Cliccando su Stampa si confermerà l'operazione.

![](<../../.gitbook/assets/image (77) (1) (1) (1) (1) (1) (1) (1) (1).png>)

Si aprirà quindi ora la stampa del riepilogo degli interventi selezionati.

![](<../../.gitbook/assets/image (94) (1) (1).png>)

### 📱 Sincronizzazione degli interventi APP tecnici

Con OpenSTAManager è possibile sincronizzare le attività con il calendario del proprio telefono tramite l'apposita App.

![](<../../.gitbook/assets/image (56) (1) (1) (1) (1) (1) (1) (1).png>)

Per i dettagli su come configurare l'App tecnici consultare l'[apposita guida](../../esempi/calendario-su-telefono.md).

## 👤 Dal dettaglio Attività

Cliccando su uno specifico record è possibile entrare nella schermata di dettaglio.\
Da qui, nella sezione superiore della pagina, è possibile trovare le funzioni:

* Stampa Intervento
* Invio del rapportino intervento via email
* Duplica attività
* Visualizzazione dell'anteprima della stampa e [firma conclusiva dell'attività](modifica.md#anteprima-e-firma)

### 🖨️ Stampa intervento

Dalla schermata di dettaglio di un'attività è possibile procedere a diversi tipi di stampe:

* Stampa intervento e checklist
* Stampa intervento e checklist (senza prezzi)
* Stampa intervento (senza prezzi)
* Stampa intervento

![](<../../.gitbook/assets/image (92) (1) (2) (1) (1) (1) (1).png>)

Cliccando sul tipo di stampa scelto sarà possibile visualizzare la stampa del documento

![](<../../.gitbook/assets/image (79) (1) (1) (1) (1).png>)

### ✉️ Invio del rapportino intervento

Dalla schermata di dettaglio di un'attività è possibile procedere a inviare diversi documenti via mail:

* Rapportino intervento
* Notifica intervento
* Notifica rimozione intervento
* Notifica stato intervento

![](<../../.gitbook/assets/image (25) (1) (1) (1).png>)

Cliccando sul tipo di documento da inviare si verrà indirizzati al template email compilato con i dati dell'attività, dove sarà possibile inviare la mail cliccando su Invia.

![](<../../.gitbook/assets/image (67) (1) (1) (1) (1) (1) (1) (1).png>)

### 🧬 Duplica attività

Dalla schermata di dettaglio di un'attività è possibile procedere alla sua duplicazione cliccando su duplica attività.

![](<../../.gitbook/assets/image (46) (1) (1).png>)

### 🖊️ Anteprima e firma

Dalla schermata di dettaglio di un'attività è possibile procedere alla visualizzazione della sua anteprima da far firmare al cliente per segnalare l'avvenuto completamente.

![](<../../.gitbook/assets/image (33) (1) (2).png>)

Una volta che il cliente avrà firmato e cliccato su Salva firma, verrà registrata e sarà impossibile modificarla.

![](<../../.gitbook/assets/image (96) (1) (1) (1) (1) (1) (1).png>)

La firma salvata è visualizzabile a fondo pagina dalla schermata di dettaglio del record.

![](<../../.gitbook/assets/image (73) (1) (1) (1) (1).png>)
