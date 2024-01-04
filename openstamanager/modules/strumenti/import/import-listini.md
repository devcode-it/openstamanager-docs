---
description: Come importare listini in OpenSTAManager
---

# 📥 Import Listini

{% hint style="info" %}
È possibile importare i listini degli articoli in maniera massiva tramite il caricamento di un file CSV.
{% endhint %}

Accedere al modulo Strumenti/[Import](./) e impostare **Articoli** nel menù a tendina.

Dopo aver selezionato il modulo sarà visibile un nuovo pulsante nella schermata "Scarica esempio CSV".

<figure><img src="../../../../.gitbook/assets/immagine (715).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
L'importazione dei listini avviene tramite la procedura di importazione degli articoli, le specifiche da seguire sono quindi le stesse.
{% endhint %}

{% hint style="warning" %}
Nel file CSV va utilizzato come separatore il carattere _;_ (punto e virgola).
{% endhint %}

{% content-ref url="import-articoli.md" %}
[import-articoli.md](import-articoli.md)
{% endcontent-ref %}

{% hint style="danger" %}
In caso di articolo esistente, in fase di import TUTTI i campi mappati andranno a sovrascrivere i campi presenti anche se nel file CSV la colonna è vuota, è necessario quindi non mappare le colonne da non sovrascrivere.
{% endhint %}

Pertanto nel caricamento di un CSV con i dati listino, consigliamo di compilare e mappare unicamente i dati relativi al listino da importare, per non modificare gli articoli presenti.

Questi campi sono:

* Codice\*
* Anagrafica listino\*
* Codice fornitore\*
* Barcode fornitore
* Descrizione fornitore\*
* Qta minima
* Qta massima
* Prezzo listino\*
* Sconto listino
* Cliente/Fornitore listino\*

{% hint style="info" %}
I campi contrassegnati dall'asterisco \* sono obbligatori.
{% endhint %}
