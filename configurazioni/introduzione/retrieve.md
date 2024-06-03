# 📙 Retrieve

Le operazioni di _retrieve_ permettono di ottenere le informazioni registrate nel gestionale, e solitamente non influenzano in alcun modo lo stato del software e i dati interni.

{% hint style="warning" %}
In base alle capacità del server in cui il gestionale è installato, è possibile un rallentamento del server in caso di molteplici richieste contemporanee all'API.
{% endhint %}

### 📙 Standard di funzionamento

Considerando la potenziale quantità delle informazioni restituite, il sistema API del gestionale restituisce le informazioni richieste presentando una paginazione di default di 200 record (impostazione _Lunghezza pagine per API_).

## Richiesta standard

<mark style="color:blue;">`GET`</mark> `http://localhost/openstamanager/api?token=<token>&resource=<resource>`

Richiesta standard per la comunicazione con l'API in modalità

_retrieve_

.

#### Query Parameters

| Name     | Type    | Description                                                                                                                                                    |
| -------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| token    | string  | Token di accesso                                                                                                                                               |
| resource | string  | Risorsa richiesta                                                                                                                                              |
| page     | integer | <p>Intero compreso tra 0 e il valore del campo</p><p><code>pages</code></p><p>restituito dalla prima richiesta (esempio:</p><p><code>page=5</code></p><p>)</p> |
| display  | array   | <p>Array che indica un filtro sui campi da restituire alla richiesta (esempio:</p><p><code>display=[id,name]</code></p><p>)</p>                                |
| filter   | array   | <p>Array composto che indica dei filtro da applicare sui contenuti dei risultati alla richiesta (esempio:</p><p><code>filter[id]=[1]</code></p><p>)</p>        |
| order    | array   | Array che indica l'ordinamento da impostare sulla richiesta                                                                                                    |

{% tabs %}
{% tab title="200 " %}
```
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Il rispetto delle opzioni sopra indicate, come per la gestione della paginazione automatica, è riservato alla singola risorsa: in casi specifici e documentati, la risorsa potrebbe ignorare le opzioni indicate a favore di un comportamento personalizzato.

Questo è particolarmente rilevante in caso di personalizzazioni, interne o esterne, del software.
{% endhint %}

### 📙 Risorse disponibili

* Anagrafiche: `anagrafiche`
* Interventi: `interventi`
