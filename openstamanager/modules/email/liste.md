---
description: Come creare una lista di utenti in OpenSTAManager
icon: circle
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/UK4SVx7wuArwVldJWR1I/openstamanager/modules/email/liste
---

# Liste

{% hint style="info" %}
Il modulo **Liste** permette all’azienda di creare dei gruppi di destinatari da utilizzare nell' invio delle **email.**
{% endhint %}

Questo modulo è complementare a [Newsletter](newsletter.md), che si occupa dell'invio email a più destinatari.

Il modulo si presenta così:

<figure><img src="../../../.gitbook/assets/immagine (252).png" alt=""><figcaption></figcaption></figure>

## Creazione

E' possibile creare una nuova lista premendo sul tasto (+):

<figure><img src="../../../.gitbook/assets/immagine (253).png" alt=""><figcaption></figcaption></figure>

## Modifica

Dalla schermata di dettaglio è possibile completare tutte le informazioni riguardanti la lista, e modificare le informazioni presenti.

Sono qui disponibili i seguenti attributi:

* **Descrizione**: In questo campo è possibile aggiungere o aggiornare la descrizione della lista.
* **Query dinamica:** L'utilizzo di questo campo esclude la possibilità di inserire i destinatari tramite il menù a tendina "_Destinatari"_ presente nella sezione Aggiunta destinatari.\
  Le informazioni inserite in questo campo devono essere scritte con il linguaggio sql;\
  &#xNAN;_&#x45;sempio_: "SELECT idanagrafica AS id, 'Modules\Anagrafiche\Anagrafica' AS tipo FROM an\_anagrafiche WHERE deleted\_at IS NUL&#x4C;**"** aggiungerà tutte le anagrafiche nella tabella Destinatari.
* **Destinatari:** In alternativa, lasciando vuoto il campo _Query dinamica_ è possibile aggiungere i vari destinatari tramite il menù a tendina, cliccando su aggiungi infatti, verranno inseriti i destinatari sulla tabella corrispondente.

{% hint style="warning" %}
Questo è uno strumento avanzato, è infatti necessario sapere come formulare le query.
{% endhint %}

<figure><img src="../../../.gitbook/assets/immagine (1304).png" alt=""><figcaption></figcaption></figure>

Selezionando una tipologia di anagrafica nel campo Tipologia e cliccando su Genera, è possibile generare la relativa query dinamica, che estrae le anagrafiche appartenenti a quella determinata tipologia.

<figure><img src="../../../.gitbook/assets/immagine (1305).png" alt=""><figcaption></figcaption></figure>

