---
description: Come importare attività in OpenSTAManager
icon: circle
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/UK4SVx7wuArwVldJWR1I/openstamanager/modules/strumenti/import/import-attivita
---

# Import Attività

{% hint style="info" %}
È possibile importare le attività in maniera massiva tramite il caricamento di un file CSV.
{% endhint %}

Accedere dal menù di OpenSTAManager al modulo Strumenti/[Import](./) e impostare **Attività** nel menù a tendina, dopo aver selezionato il modulo sarà visibile un nuovo pulsante nella schermata "Scarica esempio CSV".

Cliccando su questo pulsante si aprirà un file di esempio di come impostare il file CSV per l'importazione delle attività.

<figure><img src="../../../../.gitbook/assets/image (793).png" alt=""><figcaption></figcaption></figure>

A questo punto si può iniziare a creare il file CSV per l'importazione delle attività, seguendo la base del file d'esempio.

{% hint style="warning" %}
Nel file CSV va utilizzato come separatore il carattere _;_ (punto e virgola).
{% endhint %}

{% hint style="danger" %}
Per procedere all'importazione di attività collegate ad impianti è necessario che la matricola indicata sia già censita in impianti. Procedere quindi prima all'importazione degli impianti e successivamente delle attività.
{% endhint %}

{% hint style="danger" %}
La ricerca dell'anagrafica da collegare all'attività avviene sulla base della partita iva o del codice fiscale mappato.&#x20;

Per procedere all'importazione dell'attività è pertanto necessario che almeno uno dei due valori siano censito in anagrafica.&#x20;
{% endhint %}

Una volta completato il file si può procedere al suo caricamento, andando a selezionarlo da Sfoglia e cliccando poi su Aggiungi.

<figure><img src="../../../../.gitbook/assets/image (794).png" alt=""><figcaption></figcaption></figure>

Da questa schermata sarà ora possibile procedere a mappare i campi del CSV con quelli del gestionale, impostare la chiave primaria e cliccare su Avvia importazione.

I campi mappabili a database sono:

* codice
* telefono
* data
* data richiesta
* ora inizio
* ora fine
* tecnico
* tipo
* note
* impianto
* richiesta
* descrizione
* stato

E' presente in fase di importazione un automatismo che genera automaticamente i valori dei seguenti campi se mappati:

* la sessione del tecnico se mappato l'orario di inizio attività
* lo stato attività, se non è già presente a gestionale

{% hint style="warning" %}
In caso di attività esistente, in fase di import TUTTI i campi mappati andranno a sovrascrivere i campi presenti anche se nel file CSV la colonna è vuota, è necessario quindi non mappare le colonne da non sovrascrivere
{% endhint %}
