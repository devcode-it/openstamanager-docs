---
title: API
sidebar:
  nav: docs-sidebar
---

# API

> Con application programming interface \(in acronimo API, in italiano interfaccia di programmazione di un'applicazione\), in informatica, si indica ogni insieme di procedure disponibili al programmatore, di solito raggruppate a formare un set di strumenti specifici per l'espletamento di un determinato compito all'interno di un certo programma.
>
> [Wikipedia](https://it.wikipedia.org/wiki/Application_programming_interface)

L'API del progetto è attualmente ancora in sviluppo, e pertanto le funzioni disponibili potrebbero essere piuttosto ridotte. Di seguito sono elencate le basi per connettersi al sistema e ottenere i dati a cui si è interessati.

## Requisiti aggiuntivi

Per rendere la gestione dell'API maggiormente mantenibile e unificata, il suo funzionamento è stato sottoposto al seguente requisito aggiuntivo:

* MySQL &gt;= 5.6.5

Se queste requisito non viene soddisfatto, l'installazione del gestionale procederà correttamente, ma i tentativi di connessione con l'API saranno rifiutati con il codice di errore `503` e lo stato `Servizio non disponibile`.

Nel caso, a seguito dell'installazione di OpenSTAManager, venisse aggiornato il servizio MySQL per permettere il funzionamento dell'API, sarà necessaro causare l'esecuzione della procedura di aggiornamento del gestionale, che organizzarà correttamente il database per la compatibilità con l'API.

**Attenzione**: il solo aggiornamento del servizio MySQL senza il successivo aggiornamento del gestionale potrebbe causare malfunzionamenti di vario genere nell'utilizzo dell'API. 

## Standard di comunicazione

Il funzionamento dell'API si basa fondamentalmente sull'utilizzo di una chiave di accesso univoca per ogni dispositivo, ospitata all'interno della tabella `zz_tokens` del database del progetto.

Ogni richiesta all'API deve contenere la chiave di accesso \(campo `token`\) e l'operazione richiesta \(campo `resource`\), inserendo questi elementi tra gli ulteriori contenuti che si intendono inviare. I contenuti della richiesta devono quindi essere convertiti in formato JSON ed inviati all'API secondo uno specifico schema:

* `POST` - Richieste di creazione \(**Create**\).
* `GET` - Richieste di informazioni \(**Retrieve**\).
* `PUT` - Richieste di modifica \(**Update**\).
* `DELETE` - Richieste di eliminazione \(**Delete**\).

### Ottenere la chiave

La chiave di accesso può essere ottenuta sfruttando l'operazione di accesso nativa dell'API, che prevede l'invio di una richiesta **POST** corrispondente alla seguente struttura:

* `resource` - login.
* `username` - &lt;username dell'account&gt;.
* `password` - &lt;password dell'account&gt;.

### Formato dei componenti

I seguenti componenti delle richieste devono seguire una rigida struttura:

* `page` - intero.
* `upd` - yyyy-MM-dd hh:mm:ss.

## Output

L'API del progetto permette di ottenere le informazioni attraverso un array in formato JSON.

### Stati

Ogni richiesta effettuata all'API viene accompagnata da un messaggio predefinito che permette di interpretare in modo più preciso la risposta. In particolare, sono presenti i seguenti _status_:

* `200: OK` - La richiesta è andata a buon fine.
* `400: Errore interno dell'API` - La richiesta effettuata risulta invalida per l'API.
* `401: Non autorizzato` - Accesso non autorizzato.
* `404: Non trovato` - La risorsa richiesta non risulta disponibile.
* `500: Errore del server` - Il gestionale non è in grado di completare la richiesta.
* `503: Servizio non disponibile` - L'API del gestionale non è abilitata.

### Lettura

Le richieste di lettura sono solitamente completate con un numero predefinito di informazioni. Per poter interpretare correttamente i dati, si devono sfruttare in particolare i seguenti campi generici:

* `records`: elenco dei record presenti nella pagina richiesta \(parametro `page`\);
* `total-count`: numero totale dei record;
* `pages`: numero della pagine disponibili.

Si ricorda che l'API prevede la restituzione di un insieme di dati limitato rispetto alla richiesta effettuatua: per ottenere l'intero insieme di informazioni è necessario eseguire molteplici richieste consecutive basate sul campo `page`.

La lunghezza delle pagine dell'API viene definita dall'impostazione _Lunghezza pagine per API_, modificabile esclusivamente all'interno della tabella `zz_settings`.

## Personalizzazione

L'API sfrutta una struttura modulare per poter funzionare in modo completo e garantire al tempo stesso il possibile ampliamento delle sue funzioni. In particolare, ogni modulo può specificare una determinata serie di operazioni che lo riguardano e che possono essere richiamate in vari modi.

Di seguito lo schema attraverso cui l'API individua la presenza delle possibili richieste supportate dai moduli \(cartelle **api/** e **custom/api/**\):

* `POST` - File `create.php`.
* `GET` - File `retrieve.php`.
* `PUT` - File `update.php`.
* `DELETE` - File `delete.php`.

## Richieste di lettura

### Interventi

Tutto il contenuto della tabella in\_interventi:

```text
http://<url_osm>/api/?token=<token>&resource=in_interventi
```

Singolo intervento \(riga della tabella\):

```text
http://<url_osm>/api/?token=<token>&resource=in_interventi&filter[id]=[1]
```

### Anagrafiche

Tutto il contenuto della tabella an\_anagrafiche:

```text
http://<url_osm>/api/?token=<token>&resource=an_anagrafiche
```

Singolo intervento \(riga della tabella\):

```text
http://<url_osm>/api/?token=<token>&resource=an_anagrafiche&filter[idanagrafica]=[1]
```

Ricerca per ragione sociale:

```text
http://<url_osm>/api/?token=<token>&resource=an_anagrafiche&filter[ragione_sociale]=[%<stringa_ragione_sociale>%]
```

### Richieste disabilitate

#### Modifiche

Tutti i contenuti di tutte le tabelle:

```text
http://<url_osm>/api/?token=<token>&resource=updates
```

Tutti i contenuti di tutte le tabelle, aggiornati a partire da una data precisa:

```text
http://<url_osm>/api/?token=<token>&resource=updates&upd=2016-01-31%2010:44:31
```

#### Eliminazioni

Tutte le eliminazioni di tutte le tabelle:

```text
http://<url_osm>/api/?token=<token>&resource=deleted
```

