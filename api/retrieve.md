# Retrieve

Le operazioni di _retrieve_ permettono di ottenere le informazioni registrate nel gestionale, e solitamente non influenzano in alcun modo lo stato del software e i dati interni.

{% hint style="warning" %}
In base alle capacità del server in cui il gestionale è installato, è possibile un rallentamento del server in caso di molteplici richieste contemporanee all'API.
{% endhint %}

### Standard di funzionamento

Considerando la potenziale quantità delle informazioni restituite, il sistema API del gestionale restituisce le informazioni richieste presentando una paginazione di default di 200 record \(impostazione _Lunghezza pagine per API_\).

{% api-method method="get" host="http://localhost/openstamanager" path="/api?token=<token>&resource=<resource>" %}
{% api-method-summary %}
Richiesta standard
{% endapi-method-summary %}

{% api-method-description %}
Richiesta standard per la comunicazione con l'API in modalità _retrieve_.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
Token di accesso
{% endapi-method-parameter %}

{% api-method-parameter name="resource" type="string" required=true %}
Risorsa richiesta
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="integer" required=false %}
Intero compreso tra 0 e il valore del campo `pages` restituito dalla prima richiesta \(esempio: `page=5`\)
{% endapi-method-parameter %}

{% api-method-parameter name="display" type="array" required=false %}
Array che indica un filtro sui campi da restituire alla richiesta \(esempio: `display=[id,name]`\)
{% endapi-method-parameter %}

{% api-method-parameter name="filter" type="array" required=false %}
Array composto che indica dei filtro da applicare sui contenuti dei risultati alla richiesta \(esempio: `filter[id]=[1]`\)
{% endapi-method-parameter %}

{% api-method-parameter name="order" type="array" required=false %}
Array che indica l'ordinamento da impostare sulla richiesta
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Il rispetto delle opzioni sopra indicate, come per la gestione della paginazione automatica, è riservato alla singola risorsa: in casi specifici e documentati, la risorsa potrebbe ignorare le opzioni indicate a favore di un comportamento personalizzato.

Questo è particolarmente rilevante in caso di personalizzazioni, interne o esterne, del software.
{% endhint %}

### Risorse disponibili

* Anagrafiche: `anagrafiche`
* Interventi: `interventi`

