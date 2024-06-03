---
description: Come importare articoli in OpenSTAManager
---

# 📥 Import Articoli

{% hint style="info" %}
È possibile importare gli articoli in maniera massiva tramite il caricamento di un file CSV.
{% endhint %}

Accedere dal menù di OpenSTAManager al modulo Strumenti/[Import](./) e impostare **Articoli** nel menù a tendina, dopo aver selezionato il modulo sarà visibile un nuovo pulsante nella schermata "Scarica esempio CSV".

Cliccando su questo pulsante si aprirà un file di esempio di come importare gli articoli e i listini tramite il file CSV.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2Fe7Aad6qn1TB3J72HMwdI%2Ffile.png?alt=media)

A questo punto si può iniziare a creare il file CSV per l'importazione degli articoli, seguendo la base del file d'esempio.

{% hint style="warning" %}
Gli importi inseriti devono avere come separatore il punto, e presentare due decimali.\
ad esempio per inserire come valore 2,50 si dovrà inserire **2.50**\
per inserire come valore 3 si dovrà inserire **3.00**\
per inserire come valore 54356,983 si dovrà inserire **54356.98**
{% endhint %}

{% hint style="info" %}
Se l'impostazione **Utilizza prezzi di vendita comprensivi di IVA** è abilitata, il campo mappato come prezzo di vendita corrisponderà al prezzo di vendita **ivato**.
{% endhint %}

{% hint style="warning" %}
Nel file CSV va utilizzato come separatore il carattere _;_ (punto e virgola).
{% endhint %}

Una volta completato il file si può procedere al suo caricamento, andando a selezionarlo da Sfoglia e cliccando poi su Aggiungi.

<figure><img src="../../../../.gitbook/assets/immagine (506).png" alt=""><figcaption></figcaption></figure>

Da questa schermata sarà ora possibile procedere a mappare i campi del CSV con quelli del gestionale, impostare la chiave primaria e cliccare su Avvia importazione.

I campi mappabili a database sono:

* codice
* immagine
* import immagine \*
* descrizione
* quantità
* data inventario
* unità di misura
* prezzo di acquisto
* prezzo di vendita
* peso lordo
* volume
* categoria
* sottocategoria
* barcode
* fornitore predefinito
* partita iva
* codice iva di vendita
* ubicazione
* note
* anagrafica listino
* codice fornitore
* barcode fornitore
* descrizione fornitore
* quantità massima
* quantità minima
* prezzo di listino
* sconto di listino
* direzione listino (Cliente o Fornitore)
* sede&#x20;

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
* anagrafica listino
* listino
* dettaglio fornitore

{% hint style="warning" %}
In caso di articolo esistente, in fase di import TUTTI i campi mappati andranno a sovrascrivere i campi presenti anche se nel file CSV la colonna è vuota, è necessario quindi non mappare le colonne da non sovrascrivere.
{% endhint %}

{% hint style="danger" %}
L'importazione dell'anagrafica collegata all'articolo avviene utilizzando come chiave primaria la **Partita IVA,** e in seguito la ragione sociale se non viene trovata corrispondenza. E' opportuno pertanto indicare nel file CSV di importazione la partita IVA dell'anagrafica per associare correttamente l'anagrafica cliente/fornitore del listino.&#x20;
{% endhint %}

#### Vedi anche:&#x20;

{% content-ref url="../../../../guide/videoguide/importazione-articoli.md" %}
[importazione-articoli.md](../../../../guide/videoguide/importazione-articoli.md)
{% endcontent-ref %}
