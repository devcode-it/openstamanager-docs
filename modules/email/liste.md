# Liste



{% hint style="info" %}
Il modulo **Liste** permette all’azienda di creare dei gruppi di destinatari da utilizzare nell' invio delle **email.**
{% endhint %}

Questo modulo è complementare a [Newsletter](newsletter.md), che si occupa dell'invio email a più destinatari.

## Navigazione

Il modulo è raggiungibile attraverso il menu laterale del gestionale, sotto il link **Liste** visibile dall'espansione del menu **Gestione email**.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FcZ2KKn4BVE3EWqPYICiD%2Ffile.png?alt=media)

## Caratteristiche

La schermata principale del modulo è strutturata secondo la tabella generale predefinita.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FjyOPGay6HHqWOF8iYMU1%2Ffile.png?alt=media)

### Creazione

La creazione di nuovi elementi segue il funzionamento standard del gestionale, necessitando il click sul pulsante apposito all'interno dell'intestazione del modulo.

Viene quindi data la possibilità di inserire il nome della lista.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FQ8HXdaJR5cDoZg0fmwWr%2Ffile.png?alt=media)

### Modifica

La schermata di modifica permette il completamento di tutte le informazioni riguardanti la **Lista**.

In particolare, oltre al campo **Nome** previsto alla creazione, vengono resi disponibili i seguenti attributi:

**Descrizione** \
In questo campo è possibile aggiungere o aggiornare la descrizione della lista.

**Query dinamica**\
****L'utilizzo di questo campo esclude la possibilità di inserire i destinatari tramite il menù a tendina "_Destinatari"_ presente nella sezione Aggiunta destinatari.\
Le informazioni inserite in questo campo devono essere scritte con il linguaggio sql;\
_Esempio_:  "**SELECT idanagrafica AS id FROM an\_anagrafiche"** aggiungerà tutte le anagrafiche nella tabella Destinatari.

**Destinatari**\
In alternativa, lasciando vuoto il campo _Query dinamica_ è possibile aggiungere i vari destinatari tramite il menù a tendina, cliccando su aggiungi infatti, verranno inseriti i destinatari sulla tabella corrispondente.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2F9SgkV6IU5Xvp6HLCLSnK%2Ffile.png?alt=media)

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FJNMgVuIL6m4j9IvNhxRY%2Ffile.png?alt=media)
