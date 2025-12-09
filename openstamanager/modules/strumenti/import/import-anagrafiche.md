---
description: Come importare anagrafiche in OpenSTAManager
icon: circle
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/UK4SVx7wuArwVldJWR1I/openstamanager/modules/strumenti/import/import-anagrafiche
---

# Import Anagrafiche

{% hint style="info" %}
È possibile importare le anagrafiche in maniera massiva tramite il caricamento di un file CSV.
{% endhint %}

In Strumenti/[Import](./) è possibile scaricare un esempio di CSV impostando Anagrafiche nel campo modulo. Cliccando ora sul pulsante Scarica esempio CSV si aprirà un file di esempio di come importare le anagrafiche.

<figure><img src="../../../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/immagine (388).png" alt=""><figcaption></figcaption></figure>

A questo punto si può iniziare a creare il file CSV per l'importazione delle anagrafiche, seguendo la base del file d'esempio.

{% hint style="warning" %}
Nel file CSV va utilizzato come separatore il carattere _;_ (punto e virgola).
{% endhint %}

Una volta completato il file si può procedere al suo caricamento, andando a selezionarlo da Sfoglia e cliccando poi su Aggiungi.

Da questa schermata sarà ora possibile procedere a mappare i campi del CSV con quelli del gestionale, impostare la chiave primaria e cliccare su Avvia importazione.

I campi mappabili a database sono:

* Codice (chiave primaria di default)
* Ragione sociale
* Nome
* Cognome
* Codice destinatario
* Provincia
* Città
* Telefono
* Indirizzo
* CAP
* Cellulare
* Fax
* Email
* PEC
* Sito web
* Codice fiscale
* Data di nascita (solo per anagrafiche con Tipologia privato)
* Luogo di nascita (solo per anagrafiche con Tipologia privato)
* Sesso (solo per anagrafiche con Tipologia privato)
* Partita IVA
* IBAN
* Note
* Nazione
* ID agente
* ID pagamento
* Tipo (Cliente/Fornitore)
* Tipologia (Azienda, Privato, Ente pubblico)
* Split payment
* Settore merceologico

E' presente in fase di importazione un automatismo che genera automaticamente i valori dei seguenti campi se mappati:

* Tipo anagrafica
* Settore merceologico

{% hint style="warning" %}
In caso di anagrafica esistente, in fase di import TUTTI i campi mappati andranno a sovrascrivere i campi presenti anche se nel file CSV la colonna è vuota, è necessario quindi non mappare le colonne da non sovrascrivere.
{% endhint %}

{% hint style="info" %}
E' possibile importare le anagrafiche in base alla ragione sociale o ai campi separati  cognome e nome. Se valorizzato verrà considerato il campo ragione sociale, se non valorizzato esso assumerà il valore di 'cognome nome'.
{% endhint %}
