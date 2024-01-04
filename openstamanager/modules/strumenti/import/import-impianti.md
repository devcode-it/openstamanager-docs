---
description: Come importare impianti in OpenSTAManager
---

# 📥 Import Impianti

{% hint style="info" %}
È possibile importare gli impianti in maniera massiva tramite il caricamento di un file CSV.
{% endhint %}

Accedere dal menù di OpenSTAManager al modulo Strumenti/[Import](./) e impostare **Impianti** nel menù a tendina, dopo aver selezionato il modulo sarà visibile un nuovo pulsante nella schermata "Scarica esempio CSV".

Cliccando su questo pulsante si aprirà un file di esempio di come importare gli impianti tramite il file CSV.

<figure><img src="../../../../.gitbook/assets/immagine (9).png" alt=""><figcaption></figcaption></figure>

A questo punto si può iniziare a creare il file CSV per l'importazione degli impianti, seguendo la base del file d'esempio.

{% hint style="warning" %}
Nel file CSV va utilizzato come separatore il carattere _;_ (punto e virgola).
{% endhint %}

Una volta completato il file si può procedere al suo caricamento, andando a selezionarlo da Sfoglia e cliccando poi su Aggiungi.

<figure><img src="../../../../.gitbook/assets/immagine (10).png" alt=""><figcaption></figcaption></figure>

Da questa schermata sarà ora possibile procedere a mappare i campi del CSV con quelli del gestionale, impostare la chiave primaria e cliccare su Avvia importazione.

I campi mappabili a database sono:

* matricola
* immagine
* import immagine \*
* nome
* cliente
* telefono
* categoria
* sottocategoria
* sede
* descrizione
* data installazione

{% hint style="info" %}
**Come valorizzare Import immagine:**

1 -> permette di importare l'immagine come principale dell'articolo mantenendo gli altri allegati già presenti,

2 -> permette di importare l'immagine come principale dell'articolo rimuovendo tutti gli allegati presenti,

3 -> permette di importare l'immagine come allegato dell'articolo mantenendo gli altri allegati già presenti,

4 -> permette di importare l'immagine come allegato dell'articolo rimuovendo tutti gli allegati presenti.
{% endhint %}

E' presente in fase di importazione un automatismo che genera automaticamente i valori dei seguenti campi se mappati:

* categoria
* sottocategoria

{% hint style="warning" %}
In caso di impianto esistente, in fase di import TUTTI i campi mappati andranno a sovrascrivere i campi presenti anche se nel file CSV la colonna è vuota, è necessario quindi non mappare le colonne da non sovrascrivere.
{% endhint %}

{% hint style="danger" %}
La ricerca dell'anagrafica da collegare all'attività avviene sulla base del numero di telefono mappato, per procedere all'importazione dell'attività è pertanto necessario che il numero di telefono indicato sia censito in anagrafica. Procedere quindi prima all'importazione delle anagrafiche.
{% endhint %}

