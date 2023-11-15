# 📥 Import anagrafiche

{% hint style="info" %}
È possibile importare le anagrafiche in maniera massiva tramite il caricamento di un file CSV.
{% endhint %}

In Strumenti/[Import](./) è possibile scaricare un esempio di CSV impostando Anagrafiche nel campo modulo. Cliccando ora sul pulsante Scarica esempio CSV si aprirà un file di esempio di come importare le anagrafiche.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FKAYcjU46Mt551Js0WFWg%2Ffile.png?alt=media)

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2Fd2zONN3MJ2hKZcXEia83%2Ffile.png?alt=media)

A questo punto si può iniziare a creare il file CSV per l'importazione delle anagrafiche, seguendo la base del file d'esempio.

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
* Civico
* CAP
* Cellulare
* Fax
* Email
* Pec
* Sito web
* Codice fiscale
* Data di nascita
* Luogo di nascita
* Sesso
* Partita IVA
* Codice IBAN
* Note
* Nazione
* Agente
* Pagamento predefinito
* Tipo di anagrafica (cliente/fornitore)
* Tipologia (Privato, Ente pubblico, Azienda)
* Split payment
* Settore merceologico

E' presente in fase di importazione un automatismo che genera automaticamente i valori dei seguenti campi se mappati:

* Tipo anagrafica
* Settore merceologico

