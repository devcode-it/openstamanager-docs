---
description: Come creare una lista di utenti in OpenSTAManager
---

# 📋 Liste

{% hint style="info" %}
Il modulo **Liste** permette all’azienda di creare dei gruppi di destinatari da utilizzare nell' invio delle **email.**
{% endhint %}

Questo modulo è complementare a [Newsletter](newsletter.md), che si occupa dell'invio email a più destinatari.

Il modulo si presenta così:

<figure><img src="../../../.gitbook/assets/immagine (119).png" alt=""><figcaption></figcaption></figure>

## ➕ Creazione

E' possibile creare una nuova lista premendo sul tasto (+):

<figure><img src="../../../.gitbook/assets/immagine (120).png" alt=""><figcaption></figcaption></figure>

## 🖌️ Modifica

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

<figure><img src="../../../.gitbook/assets/immagine (121).png" alt=""><figcaption></figcaption></figure>

Ad esempio, volendo creare una lista contenente tutti i clienti che non hanno fatto ordini negli ultimi 6 mesi si dovrà compilare il campo **Query dinamica** in questo modo:

<pre class="language-bash"><code class="lang-bash">SELECT
    an_anagrafiche.idanagrafica AS id,
    'Modules\\Anagrafiche\\Anagrafica' AS tipo
FROM
    an_anagrafiche
<strong>    INNER JOIN an_tipianagrafiche_anagrafiche ON an_anagrafiche.idanagrafica = an_tipianagrafiche_anagrafiche.idanagrafica
</strong>    INNER JOIN an_tipianagrafiche ON an_tipianagrafiche_anagrafiche.idtipoanagrafica = an_tipianagrafiche.id
    LEFT JOIN an_tipianagrafiche_lang ON (an_tipianagrafiche_lang.id_record = an_tipianagrafiche.id AND an_tipianagrafiche_lang.id_lang = 1)
WHERE
    deleted_at IS NULL AND an_tipianagrafiche_lang.title = "Cliente"
</code></pre>

<figure><img src="../../../.gitbook/assets/immagine (64).png" alt=""><figcaption></figcaption></figure>
