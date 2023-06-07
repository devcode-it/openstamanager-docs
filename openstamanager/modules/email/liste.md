---
description: Come creare una lista di utenti in OpenSTAManager
---

# 📋 Liste

{% hint style="info" %}
Il modulo **Liste** permette all’azienda di creare dei gruppi di destinatari da utilizzare nell' invio delle **email.**
{% endhint %}

Questo modulo è complementare a [Newsletter](newsletter.md), che si occupa dell'invio email a più destinatari.

Il modulo si presenta così:

![](<../../../.gitbook/assets/image (262).png>)

## ➕ Creazione

E' possibile creare una nuova lista premendo sul tasto (+):

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FQ8HXdaJR5cDoZg0fmwWr%2Ffile.png?alt=media)

## 🖌️ Modifica

Dalla schermata di dettaglio è possibile completare tutte le informazioni riguardanti la lista, e modificare le informazioni presenti.

Sono qui disponibili i seguenti attributi:

* **Descrizione**: In questo campo è possibile aggiungere o aggiornare la descrizione della lista.
* **Query dinamica:** L'utilizzo di questo campo esclude la possibilità di inserire i destinatari tramite il menù a tendina "_Destinatari"_ presente nella sezione Aggiunta destinatari.\
  Le informazioni inserite in questo campo devono essere scritte con il linguaggio sql;\
  _Esempio_: "SELECT idanagrafica AS id, 'Modules\Anagrafiche\Anagrafica' AS tipo FROM an\_anagrafiche WHERE deleted\_at IS NULL**"** aggiungerà tutte le anagrafiche nella tabella Destinatari.
* **Destinatari:** In alternativa, lasciando vuoto il campo _Query dinamica_ è possibile aggiungere i vari destinatari tramite il menù a tendina, cliccando su aggiungi infatti, verranno inseriti i destinatari sulla tabella corrispondente.

![](<../../../.gitbook/assets/image (310).png>)
