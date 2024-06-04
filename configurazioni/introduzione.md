---
description: Guida alla configurazione API
---

# 📙 API

> Con application programming interface (in acronimo API, in italiano interfaccia di programmazione di un'applicazione), in informatica, si indica ogni insieme di procedure disponibili al programmatore, di solito raggruppate a formare un set di strumenti specifici per l'espletamento di un determinato compito all'interno di un certo programma.
>
> [Wikipedia](https://it.wikipedia.org/wiki/Application\_programming\_interface)

Il gestionale possiede un sistema di API basilare che permette di ottenere i dati registrati al suo interno attraverso un'interfaccia comune, oltre che di creare e aggiornare le informazioni dei vari record salvati.

{% hint style="danger" %}
Il sistema API del gestionale è attualmente in sviluppo, e pertanto le funzioni disponibili potrebbero essere piuttosto ridotte.

Le informazioni qui descritte sono valida a partire dalla versione 2.4 del gestionale.
{% endhint %}

### 📙 Metodo di accesso

L'accesso all'API viene garantito esclusivamente tramite il token personale di accesso dell'utente, individuabile nella sezione dedicata alle informazioni sull'account.

<figure><img src="../.gitbook/assets/immagine.png" alt=""><figcaption></figcaption></figure>

Cliccando sulla sezione evidenziata in rosso, si apre una pagina dedicata alla visualizzazione delle informazioni personali dell'utente e che permette la modifica della password e della foto profilo, oltre che la visualizzazione del token per l'API.

<figure><img src="../.gitbook/assets/immagine (812).png" alt=""><figcaption></figcaption></figure>

Nella sezione denominata **API** sono disponibili il token e l'URL per accedere al sistema API del gestionale.

In alternativa, è disponibile la seguente risorsa dedicata per l'accesso direttamente da API.

## Richiesta di accesso

<mark style="color:orange;">`PUT`</mark> `http://localhost/openstamanager/api`

Si ricordi che, come indicato in Modalità di utilizzo, il contenuto della richiesta deve essere formattato come JSON:

`{"resource":"login", "username": "<username>", "password", "<password>"}`

#### Request Body

| Name     | Type   | Description               |
| -------- | ------ | ------------------------- |
| resource | string | Nome della risorsa: login |
| username | string | Username dell'utente      |
| password | string | Password dell'utente      |

{% tabs %}
{% tab title="200 " %}
```
```
{% endtab %}
{% endtabs %}

### 📙 Gestione degli accessi

E' disponibile un sistema di gestione degli accessi basilare per l'amministratore del gestionale, che può abilitare l'accesso degli utenti attraverso il modulo [**Utenti e permessi**](../openstamanager/modules/strumenti/utentiepermessi.md).

{% hint style="warning" %}
Non è al momento disponibile un sistema di permessi per il sistema API, e pertanto chiunque possegga un token può accedere a tutte le informazioni che l'API rende disponibile.
{% endhint %}

### 📙 Messaggi di errore

In base allo stato dell'API e alla richiesta effettuata, è possibile che vengano restituiti dei messaggi di stato che informano l'utilizzatore del risultato della richiesta.

In particolare, sono presenti i seguenti _status_:

* `200: OK` - La richiesta è andata a buon fine.
* `400: Errore interno dell'API` - La richiesta effettuata risulta invalida per l'API.
* `401: Non autorizzato` - Accesso non autorizzato.
* `404: Non trovato` - La risorsa richiesta non risulta disponibile.
* `500: Errore del server` - Il gestionale non è in grado di completare la richiesta.
* `503: Servizio non disponibile` - L'API del gestionale non è abilitata a causa della versione troppo vecchia di MySQL (>= 5.6.5).

### 📙 Modalità di utilizzo

Ogni richiesta di comunicazione con l'API deve essere composta di una chiave di accesso e di un'operazione richiesta, e deve essere formattata secondo il formato JSON.

In base al tipo di risorsa che si desidera richiedere, sono disponibili quattro metodi HTTP per la comunicazione:

* `GET`, dedicato alle richieste di informazioni ([**Retrieve**](broken-reference)).
* `POST`, dedicato alle richieste di creazione (**Create**).
* `PUT`, dedicato alle richieste di modifica (**Update**).
* `DELETE`, dedicato alle richieste di eliminazione (**Delete**).

Maggiori informazioni sulle relative risorse disponibili sono presenti nelle prossime sezioni, oltre che all'interno della tabella `zz_api_resources` del gestionale.



Vai alla documentazione completa alle API di OpenSTAManager:

{% embed url="https://api.docs.openstamanager.com/" %}
