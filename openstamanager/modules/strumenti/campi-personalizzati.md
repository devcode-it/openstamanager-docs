---
description: Come gestire i campi personalizzati in OpenSTAManager
icon: square-sliders
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/openstamanager/modules/strumenti/campi-personalizzati
---

# Campi personalizzati

{% hint style="warning" %}
Questa funzione è di rilevanza per chi desidera personalizzare alcune delle informazioni presentate dal gestionale senza modificare in modo consistente il codice generale.
{% endhint %}

A partire dalla versione 2.4 è possibile sfruttare dei campi personalizzati per aggiungere informazioni ai moduli principali in modo dinamico.

Questi campi sono gestiti a livello di database attraverso le tabelle `zz_fields` e `zz_field_record`, che si occupano rispettivamente della gestione generale dei campi e del salvataggio dei record personalizzati. Le procedure automatiche di gestione di questi campi sono integrate nei file `actions.php`, `editor.php` e `add.php`.

E' disponibile il modulo **Campi personalizzati**, da abilitare in Viste, per la gestione dinamica di queste informazioni.

#### _**Esempio di utilizzo**_

Creare un nuovo campo personalizzati cliccando sul tasto (+).

Volendo inserire un campo "Marca" selezionabile dalla videata articoli, la sintassi da utilizzare sarà la seguente:

```
// {[ "type": "select", "label": "Marca", "name": "|name|", "values": "list=\"\": \"Nessuno\", \"ValoreUno\": \"EtichettaUno\", \"ValoreDue\": \"EtichettaDue\", \"altro\": \"Altro\"", "value":"|value|"]}
```

{% hint style="warning" %}
E' importante utilizzare i valori |name| e |value| come suggerito dalle istruzioni per il campo contenuto presenti nella parte inferiore della pagina, affinchè i record vengano salvati correttamente.
{% endhint %}

![](<../../../.gitbook/assets/image (190).png>)

Questo produrrà la creazione di un campo "Marca" all'interno dei record del modulo Articoli:

![](<../../../.gitbook/assets/image (133).png>)

{% hint style="danger" %}
I campi creati in questo modo sono difficili da gestire nelle query del gestionale.
{% endhint %}

E' possibile estrarre i valori dei campi personalizzati con il seguente codice:

```
$custom_fields = new HTMLBuilder\Manager\FieldManager();

$valore_campo = $custom_fields->getValue(['id_record' => $id_record, 'id_module' => \Models\Module::where('name', 'Nome del modulo')->first()->id], 'Nome del campo');
```
