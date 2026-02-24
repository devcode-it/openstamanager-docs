---
description: Guida all'importazione di Preventivi in OpenSTAManager
icon: circle
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/I8PynmXUVfCOtwZFC1I6/openstamanager/modules/strumenti/import/import-preventivi
---

# Import Preventivi

{% hint style="info" %}
È possibile importare i preventivi in maniera massiva tramite il caricamento di un file CSV.
{% endhint %}

Accedere dal menù di OpenSTAManager al modulo Strumenti/[Import](./) e impostare **Preventivi** nel menù a tendina, dopo aver selezionato il modulo sarà visibile un nuovo pulsante nella schermata "Scarica esempio CSV".

Cliccando su questo pulsante si aprirà un file di esempio di come importare i preventivi tramite il file CSV.

<figure><img src="../../../../.gitbook/assets/immagine (609).png" alt=""><figcaption></figcaption></figure>

A questo punto si può iniziare a creare il file CSV per l'importazione dei preventivi, seguendo la base del file d'esempio.

{% hint style="info" %}
Per importare più righe dello stesso Preventivo sarà sufficiente inserire lo stesso numero preventivo nel campo Numero, che andrà utilizzato come chiave primaria.
{% endhint %}

{% hint style="warning" %}
Gli importi inseriti devono avere come separatore il punto, e presentare due decimali.\
ad esempio per inserire come valore 2,50 si dovrà inserire **2.50**\
per inserire come valore 3 si dovrà inserire **3.00**\
per inserire come valore 54356,983 si dovrà inserire **54356.98**
{% endhint %}

Una volta completato il file si può procedere al suo caricamento, andando a selezionarlo da Sfoglia e cliccando poi su Aggiungi.

<figure><img src="../../../../.gitbook/assets/immagine (846).png" alt=""><figcaption></figcaption></figure>

Da questa schermata sarà ora possibile procedere a mappare i campi del CSV con quelli del gestionale, impostare la chiave primaria e cliccare su Avvia importazione.

I campi mappabili a database sono:

* numero
* nome preventivo
* descrizione preventivo
* cliente
* tipo attività
* data
* codice articolo
* quantità riga
* data prevista evasione riga
* prezzo unitario riga

E' presente in fase di importazione un automatismo che genera automaticamente i valori dei seguenti campi se mappati:

* anagrafica
* articolo
