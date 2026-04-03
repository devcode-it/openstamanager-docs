---
description: Come gestire le Fatture di vendita in OpenSTAManager
icon: circle
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/openstamanager/modules/vendite/fatturedivendita
---

# Fatture di vendita

{% hint style="info" %}
Il modulo **Fatture di vendita** permette di gestire la fatturazione in uscita dell'azienda.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/immagine (77).png" alt=""><figcaption></figcaption></figure>

## Avvisi

Nel caso siano presenti delle fatture di vendita **generate** ma non ancora inviate (entro i 12 giorni dalla scadenza per inviare le fatture allo SDI), verranno segnalate dal gestionale con un avviso nella sezione fatture di vendita.

<figure><img src="../../../../.gitbook/assets/immagine (78).png" alt=""><figcaption></figcaption></figure>

Verranno notificare anche le fatture che invece risulteranno **scartate** dallo SDI e andranno quindi corrette e riemesse.

<figure><img src="../../../../.gitbook/assets/immagine (79).png" alt=""><figcaption></figcaption></figure>

## Creazione

Per creare una nuova Fattura di vendita si dovrà cliccare sul tasto (+).

Andranno qui inserite le informazioni relative alla nuova fattura di vendita:

* Data
* Cliente
* Tipo documento
* Sezionale

<figure><img src="../../../../.gitbook/assets/immagine (80).png" alt=""><figcaption></figcaption></figure>

## Modifica

Cliccando sul record da modificare si aprirà la schermata di dettaglio, da cui sarà possibile modificare:

* Cliente
* Agente di riferimento
* Referente
* Numero fattura
* Data emissione
* Data competenza
* Sede partenza
* Sede destinazione
* Tipo documento
* Pagamento
* Banca accredito
* Banca addebito
* Split payment
* Fattura per conto terzi
* Sconto in fattura
* Ritenuta previdenziale
* Dichiarazione d'intento
* Marca da bollo automatica
  * Addebita marca da bollo
  * Importo marca da bollo
* Note
* Note interne

<figure><img src="../../../../.gitbook/assets/immagine (81).png" alt=""><figcaption></figcaption></figure>

* Righe, che possono includere:
  * Articolo
  * Riga generica
  * Descrizione
  * Sconto/maggiorazione
  * Attività
  * Preventivo
  * Contratto
  * DDT
  * Ordine
* Allegati

<figure><img src="../../../../.gitbook/assets/immagine (1144).png" alt=""><figcaption></figcaption></figure>

## Operazioni massive sulle righe

E' possibile intervenire massivamente sulle righe dei documenti selezionandole e ricorrendo alle azioni di gruppo:

<figure><img src="../../../../.gitbook/assets/immagine (983).png" alt=""><figcaption></figcaption></figure>

* Duplica
* Elimina
* Confronta prezzi
* Aggiorna prezzi
* Modifica IVA

### Confronta prezzi

Tramite questa funzione è possibile visualizzare il prezzo utilizzato per gli articoli selezionati nell'ultimo documento e nell'ultimo preventivo.&#x20;

Da qui è possibile modificare il prezzo di vendita massivamente apportando le dovute correzioni e cliccando su **Modifica**.

<figure><img src="../../../../.gitbook/assets/immagine (897).png" alt=""><figcaption></figcaption></figure>



## Plugin

Selezionando uno specifico record si può accedere a diversi plugin nella barra laterale della pagina:

* Fatturazione elettronica
* Movimenti contabili
* Registrazioni
* Note interne
* Info

Dalla schermata del modulo è invece possibile accedere al plugin [RicevuteFE](ricevute-fe.md).



## Informazioni aggiuntive

{% content-ref url="plugin.md" %}
[plugin.md](plugin.md)
{% endcontent-ref %}

{% content-ref url="plugin-1/" %}
[plugin-1](plugin-1/)
{% endcontent-ref %}

{% content-ref url="../../../../guide/esempi/autofattura.md" %}
[autofattura.md](../../../../guide/esempi/autofattura.md)
{% endcontent-ref %}

{% content-ref url="../../../../guide/esempi/gestione-acconto.md" %}
[gestione-acconto.md](../../../../guide/esempi/gestione-acconto.md)
{% endcontent-ref %}

{% content-ref url="../../../../guide/esempi/nota-di-credito.md" %}
[nota-di-credito.md](../../../../guide/esempi/nota-di-credito.md)
{% endcontent-ref %}

{% content-ref url="../../../../guide/esempi/prezzo-di-vendita-automatico.md" %}
[prezzo-di-vendita-automatico.md](../../../../guide/esempi/prezzo-di-vendita-automatico.md)
{% endcontent-ref %}
