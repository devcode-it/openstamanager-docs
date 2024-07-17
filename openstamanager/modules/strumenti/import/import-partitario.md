---
description: Come importare il piano dei conti in OpenSTAManager
---

# 📥 Import Piano dei conti

{% hint style="info" %}
È possibile importare il proprio piano dei conti personalizzato in maniera massiva tramite il caricamento di un file CSV.
{% endhint %}

Accedere dal menù di OpenSTAManager al modulo Strumenti/[Import](./) e impostare **Piano dei conti** nel menù a tendina, dopo aver selezionato il modulo sarà visibile un nuovo pulsante nella schermata "Scarica esempio CSV".

Cliccando su questo pulsante si aprirà un file di esempio di come importare il piano dei conti tramite il file CSV.

<figure><img src="../../../../.gitbook/assets/immagine (237).png" alt=""><figcaption></figcaption></figure>

A questo punto si può iniziare a creare il file CSV per l'importazione del piano dei conti, seguendo la base del file d'esempio.

{% hint style="warning" %}
Nel file CSV va utilizzato come separatore il carattere _;_ (punto e virgola).
{% endhint %}

Una volta completato il file si può procedere al suo caricamento, andando a selezionarlo da Sfoglia e cliccando poi su Aggiungi.

<figure><img src="../../../../.gitbook/assets/immagine (238).png" alt=""><figcaption></figcaption></figure>

Da questa schermata sarà ora possibile procedere a mappare i campi del CSV con quelli del gestionale, impostare la chiave primaria e cliccare su Avvia importazione.

I campi mappabili a database sono:

* conto
* descrizione
* sezione
* direzione

{% hint style="warning" %}
In caso di conto esistente, in fase di import TUTTI i campi mappati andranno a sovrascrivere i campi presenti anche se nel file CSV la colonna è vuota, è necessario quindi non mappare le colonne da non sovrascrivere.
{% endhint %}

#### Vedi anche:&#x20;

{% content-ref url="../../../../guide/videoguide/importazione-articoli.md" %}
[importazione-articoli.md](../../../../guide/videoguide/importazione-articoli.md)
{% endcontent-ref %}
