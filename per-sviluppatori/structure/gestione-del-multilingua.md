# 📒 Gestione del multilingua

Dalla versione 2.5 è stata ampliata la gestione del multilingua che ora include anche i record "fissi" presenti a database.

Le lingua disponibili a gestionale sono definite nella tabella zz\_langs:

<figure><img src="../../.gitbook/assets/immagine (792).png" alt=""><figcaption></figcaption></figure>

E' possibile selezionare la lingua da utilizzare nel gestionale da **Strumenti/Impostazioni/Generali/Lingua.**

Essa viene letta da codice tramite la funzione getDefault() e impostata nel core tramite la funzione setDefault():

{% embed url="https://github.com/devcode-it/openstamanager/blob/v2.5.1/core.php#L309" %}

{% embed url="https://github.com/devcode-it/openstamanager/blob/v2.5.1/src/Models/Locale.php#L39" %}

Il valore **predefined** della tabella zz\_langs non è legato alla selezione delle lingua corrente, ma è un'impostazione interna che **non va modificata**, perchè consente la corretta funzionalità delle traduzioni. Essa infatti permette di impostare il valore predefinito per la ricerca di stringhe fisse a livello di codice tramite la funzione getPredefined().

Questo valore viene definito nel core da setPredefined():

{% embed url="https://github.com/devcode-it/openstamanager/blob/v2.5.1/core.php#L310" %}

{% embed url="https://github.com/devcode-it/openstamanager/blob/v2.5.1/src/Models/Locale.php#L49" %}

Con la nuova gestione delle lingue per ogni tabella che contiene un valore testuale è presente una corrispondente tabella**\_lang** che contiene il riferimento all'id\_record del record da tradurre, l'id\_lang che corrisponde alla lingua, e il title ovvero la traduzione del record.

Ad esempio la tabella co\_stati\_documento conterrà l'id, name, icona e colore

<figure><img src="../../.gitbook/assets/immagine (793).png" alt=""><figcaption></figcaption></figure>

mentre la tabella co\_stati\_documento**\_lang** conterrà la traduzione in italiano con id\_lang = 1 e quella in inglese con id\_lang = 2 (come definito in zz\_langs) per ogni id\_record.

<figure><img src="../../.gitbook/assets/immagine (794).png" alt=""><figcaption></figcaption></figure>

## Utilizzo del multilingua

Per poter gestire facilmente le traduzioni a livello di codice sono state introdotte queste nuove funzioni:

### setTranslation($field, $value, $id\_lang = null)

{% embed url="https://github.com/devcode-it/openstamanager/blob/v2.5.1/src/Traits/RecordTrait.php#L117" %}

Con questa funzione è possibile impostare il valore di una traduzione nella tabella $table**\_lang** a partire dall'oggetto iniziale.&#x20;

Ad esempio, si potrà aggiornare la traduzione di uno stato documento a partire dall'oggetto $stato con:

```
$stato->setTranslation('title', $descrizione);
```

$id\_lang di default è impostato nella lingua in uso dal gestionale, per forzare l'aggiornamento della traduzione di un record in una lingua diversa da quella impostata di default è necessario passare alla funzione anche l'$id\_lang.

### getTranslation($field, $id\_lang = null)

{% embed url="https://github.com/devcode-it/openstamanager/blob/v2.5.1/src/Traits/RecordTrait.php#L143" %}

Con questa funzione è possibile leggere il valore di una traduzione nella tabella $table**\_lang** a partire dall'oggetto iniziale.

Ad esempio, per recuperare la traduzione di uno stato documento a partire dall'oggetto $stato si dovrà utilizzare:

```
$stato->getTranslation('title');
```

$id\_lang di default è impostato nella lingua in uso dal gestionale, per forzare la lettura della traduzione di un record in una lingua diversa da quella impostata di default è necessario passare alla funzione anche l'$id\_lang.

### getByField($field, $value, $id\_lang = null)

{% embed url="https://github.com/devcode-it/openstamanager/blob/v2.5.1/src/Traits/RecordTrait.php#L159" %}

Con questa funzione è possibile cercare l'id\_record corrispondente a una determinata traduzione.

Ad esempio, per recuperare l'id\_record dello stato documento "Bozza", si dovrà utilizzare:

```
$stato_bozza = (new Stato())->getByField('title', 'Bozza);
```

$id\_lang di default è impostato nella lingua in uso dal gestionale, per forzare la ricerca in un'altra lingua diversa da quella impostata di default è necessario passare alla funzione anche l'$id\_lang.
