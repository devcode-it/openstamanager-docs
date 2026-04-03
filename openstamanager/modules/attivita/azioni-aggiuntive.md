---
description: Guida alle azioni aggiuntive del modulo Attività di OpenSTAManager
icon: circle
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/WzoKFijlVGKTMgti0acZ/openstamanager/modules/attivita/azioni-aggiuntive
---

# Azioni aggiuntive

## Dal modulo Attività

Il modulo Attività presenta le seguenti funzioni:

* Vedere le attività create direttamente a calendario dal modulo [Dashboard](../dashboard/);
* Selezionare dalla checkbox a inizio riga le attività interessate e cliccando su Azioni di gruppo
  * [Cambia stato](azioni-aggiuntive.md#modifica-dello-stato-massivo)
  * [Duplica](azioni-aggiuntive.md#duplicazione-massiva)
  * [Elimina](azioni-aggiuntive.md#elimina-selezionati)
  * [Esporta stampe](azioni-aggiuntive.md#esportazione-stampe)
  * [Fattura attività](azioni-aggiuntive.md#fatturazione-massiva)
  * [Firma interventi](azioni-aggiuntive.md#firma-interventi)
  * [Invia mail](azioni-aggiuntive.md#invia-mail)
  * [Stampa riepilogo](azioni-aggiuntive.md#stampa-intervento)
* [Sincronizzare](../../../guide/esempi/calendario-su-telefono.md) gli interventi dei tecnici con calendari esterni attraverso il sistema API ufficiale.

### Vedere le attività da Dashboard

Nella Dashboard è possibile visualizzare eventi creati dal modulo Attività, per avere un maggior controllo degli interventi con la vista a calendario.

Le [attività create da calendario](../dashboard/creazione.md) si riscontreranno poi nell'elenco delle attività e sarà possibile modificarle da qui, cliccando sul rispettivo record.

![](<../../../.gitbook/assets/image (596).png>)

### Esportazione stampe

Una volta selezionati i record interessati è possibile esportare massivamente le stampe cliccando su Azioni di gruppo/Esporta stampe.

Il gestionale chiederà quindi la conferma di procedere all'esportazione in formato ZIP delle stampe delle attività selezionate.

<figure><img src="../../../.gitbook/assets/immagine (1338).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Con questa operazione i dati presenti a gestionale non subiranno modifiche.
{% endhint %}

<figure><img src="../../../.gitbook/assets/immagine (1339).png" alt=""><figcaption></figcaption></figure>

Cliccando su procedi si confermerà l'operazione.

{% content-ref url="../../../guide/esempi/esportare-e-stampare-tabelle-con-molti-record.md" %}
[esportare-e-stampare-tabelle-con-molti-record.md](../../../guide/esempi/esportare-e-stampare-tabelle-con-molti-record.md)
{% endcontent-ref %}

### Fatturazione massiva

Una volta selezionati i record interessati è possibile fatturare massivamente le attività cliccando su Azioni di gruppo/Fattura interventi.

<figure><img src="../../../.gitbook/assets/immagine (1340).png" alt=""><figcaption></figcaption></figure>

Il gestionale chiederà quindi la conferma a procedere alla fatturazione, permettendo di scegliere:

* Se aggiungere le righe degli interventi selezionati a una fattura di vendita in bozze dello stesso cliente
* il sezionale in cui andare a registrare le fatture di vendita
* il tipo di documento che si andrà a creare

Cliccando su procedi si confermerà la fatturazione.

<figure><img src="../../../.gitbook/assets/immagine (1341).png" alt=""><figcaption></figcaption></figure>

Sarà ora possibile visualizzare la fattura di vendita appena creata nel modulo Vendite/Fatture di vendita, e analizzandola nel dettaglio si troveranno tra le righe le specifiche dei tre interventi svolti.

<figure><img src="../../../.gitbook/assets/immagine (198).png" alt=""><figcaption></figcaption></figure>

### Modifica dello stato massivo

Una volta selezionati i record interessati è possibile modificarne lo stato massivamente cliccando su Azioni di gruppo/Cambia stato.

<figure><img src="../../../.gitbook/assets/immagine (1343).png" alt=""><figcaption></figcaption></figure>

Il gestionale chiederà quindi la conferma a procedere alla modifica dello stato, permettendo di scegliere tra gli stati presenti:

* Completato
* Da programmare
* Fatturato
* Programmato
* (eventuali stati personalizzati)

<figure><img src="../../../.gitbook/assets/immagine (1344).png" alt=""><figcaption></figcaption></figure>

Cliccando su Procedi si confermerà l'operazione.

### Duplicazione massiva

Una volta selezionati i record interessati è possibile duplicarli massivamente cliccando su Azioni di gruppo/Duplica attività.

<figure><img src="../../../.gitbook/assets/immagine (1345).png" alt=""><figcaption></figcaption></figure>

Il gestionale chiederà quindi la conferma a procedere alla duplicazione dei record, permettendo di scegliere:

* La data e ora della richiesta
* Lo [stato](statidiattivita.md) in cui impostare i record che verranno creati
* Se duplicare anche le righe dei record selezionati
* Se duplicare anche le sessioni dei record selezionati

Cliccando su Procedi il gestionale procederà alla duplicazione.

<figure><img src="../../../.gitbook/assets/immagine (1346).png" alt=""><figcaption></figcaption></figure>

Si potranno ora vedere tra le attività i record appena creati.

![](<../../../.gitbook/assets/image (141).png>)

### Stampa massiva

Una volta selezionati i record interessati è possibile stamparli massivamente cliccando su Azioni di gruppo/Stampa riepilogo.

<figure><img src="../../../.gitbook/assets/immagine (1347).png" alt=""><figcaption></figcaption></figure>

Il gestionale chiederà quindi la conferma a procedere alla stampa dei record, permettendo di scegliere tra:

* Riepilogo clienti (con costi addebitati al cliente)
* Riepilogo interno (con costi interni del tecnico)

Cliccando su Stampa si confermerà l'operazione.

<figure><img src="../../../.gitbook/assets/immagine (1348).png" alt=""><figcaption></figcaption></figure>

Si aprirà quindi ora la stampa del riepilogo degli interventi selezionati.

<figure><img src="../../../.gitbook/assets/immagine (1349).png" alt=""><figcaption></figcaption></figure>

### &#x20;Invia mail

Con questa funzionalità è possibile inviare massivamente il tipo di documento selezionato:

<figure><img src="../../../.gitbook/assets/immagine (1350).png" alt=""><figcaption></figcaption></figure>

### Firma interventi

Con questa funzionalità è possibile firmare massivamente gli interventi

<figure><img src="../../../.gitbook/assets/immagine (1351).png" alt=""><figcaption></figcaption></figure>

### Elimina selezionati

Con questa funzionalità è possibile eliminare massivamente gli interventi

### Sincronizzazione degli interventi APP tecnici

Con OpenSTAManager è possibile sincronizzare le attività con il calendario del proprio telefono tramite l'apposita App.

![](<../../../.gitbook/assets/image (580).png>)

Per i dettagli su come configurare l'App tecnici consultare l'[apposita guida](../../../guide/esempi/calendario-su-telefono.md).

## Dal dettaglio Attività

Cliccando su uno specifico record è possibile entrare nella schermata di dettaglio.\
Da qui, nella sezione superiore della pagina, è possibile trovare le funzioni:

* Stampa
* Invio del rapportino intervento via email
* Duplica attività
* Visualizzazione dell'anteprima della stampa e [firma conclusiva dell'attività](modifica.md#anteprima-e-firma)

### Stampa intervento

Dalla schermata di dettaglio di un'attività è possibile procedere a diversi tipi di stampe:

* Stampa intervento e checklist
* Stampa intervento e checklist (senza prezzi)
* Stampa intervento (senza prezzi)
* Stampa intervento



Cliccando sul tipo di stampa scelto sarà possibile visualizzare la stampa del documento

<figure><img src="../../../.gitbook/assets/immagine (1353).png" alt=""><figcaption></figcaption></figure>

### Invio del rapportino intervento

Dalla schermata di dettaglio di un'attività è possibile procedere a inviare diversi documenti via mail:

* Rapportino intervento
* Notifica intervento
* Notifica rimozione intervento
* Notifica stato intervento

<figure><img src="../../../.gitbook/assets/immagine (207).png" alt=""><figcaption></figcaption></figure>

Cliccando sul tipo di documento da inviare si verrà indirizzati al template email compilato con i dati dell'attività, dove sarà possibile inviare la mail cliccando su Invia.

<figure><img src="../../../.gitbook/assets/immagine (206).png" alt=""><figcaption></figcaption></figure>

### Duplica attività

Dalla schermata di dettaglio di un'attività è possibile procedere alla sua duplicazione cliccando su duplica attività.

<figure><img src="../../../.gitbook/assets/immagine (208).png" alt=""><figcaption></figcaption></figure>

### Anteprima e firma

Dalla schermata di dettaglio di un'attività è possibile procedere alla visualizzazione della sua anteprima da far firmare al cliente per segnalare l'avvenuto completamente.

<figure><img src="../../../.gitbook/assets/immagine (209).png" alt=""><figcaption></figcaption></figure>

Una volta che il cliente avrà firmato e cliccato su Salva firma, verrà registrata e sarà impossibile modificarla.

<figure><img src="../../../.gitbook/assets/immagine (210).png" alt=""><figcaption></figcaption></figure>

La firma salvata è visualizzabile a fondo pagina dalla schermata di dettaglio del record.

<figure><img src="../../../.gitbook/assets/immagine (211).png" alt=""><figcaption></figcaption></figure>
