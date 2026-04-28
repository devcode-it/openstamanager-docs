---
description: Come gestire gli Articoli in OpenSTAManager
icon: circle
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/imnORsInuaaXiiRnlr6m/openstamanager/modules/magazzino/articoli-1
---

# Articoli

{% hint style="info" %}
Il modulo **Articoli** permette all’azienda di gestire le informazioni riguardanti gli articoli a magazzino, con la relativa giacenza e la gestione automatizzata dei diversi movimenti previsti all'interno di OpenSTAManager.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/immagine (61).png" alt=""><figcaption></figcaption></figure>

### Widget

* Stampa Inventario
* Valore Magazzino
* Unità di magazzino
* Stampa cespiti

<figure><img src="../../../../.gitbook/assets/immagine (62).png" alt=""><figcaption></figcaption></figure>

## Creazione

Per creare un nuovo Articolo si dovrà cliccare sul tasto (+).

Andranno qui inserite le informazioni relative al nuovo articolo:

* Codice
* Barcode (con possibilità di generarlo automaticamente)
* Descrizione
* Categoria (con possibilità di [crearla al volo](https://docs.openstamanager.com/modules/attivita/creazione#creazione-di-record-al-volo))
* Sottocategoria
* Marca
* Modello

<figure><img src="../../../../.gitbook/assets/immagine (63).png" alt=""><figcaption></figcaption></figure>

Espandendo Informazioni aggiuntive è inoltre possibile inserire:

* Prezzo di acquisto
* Coefficiente di vendita
* Prezzo di vendita
* Quantità iniziale
* Sede
* Abilitare serial number
* Unità di misura
* Unità di misura secondaria
* Fattore moltiplicativo
* Conto predefinito di acquisto
* Conto predefinito di vendita
* Iva di vendita

<figure><img src="../../../../.gitbook/assets/immagine (64).png" alt=""><figcaption></figcaption></figure>

## Modifica

Cliccando sul record da modificare si aprirà la schermata di dettaglio, in cui si troveranno diverse sezioni:

### Header

<figure><img src="../../../../.gitbook/assets/immagine (65).png" alt=""><figcaption></figcaption></figure>

### Articolo

* Immagine
* Codice
* Abilitare se si tratta di un servizio
* Attivo
* Categoria
* Sottocategoria
* Marca
* Modello
* Descrizione
* Abilitare serial number
* Ubicazione
* Unità di misura
* Garanzia
* Peso lordo
* Volume
* Unità di misura secondaria
* Fattore moltiplicativo
* Quantità multipla
* Note

<figure><img src="../../../../.gitbook/assets/immagine (67).png" alt=""><figcaption></figcaption></figure>

### Acquisto

* Prezzo di acquisto
* Fornitore predefinito
* Conto predefinito di acquisto

<figure><img src="../../../../.gitbook/assets/immagine (68).png" alt=""><figcaption></figcaption></figure>

#### Fattore moltiplicativo:

Aggiungendo nella scheda articolo un'unità di misura secondaria e il relativo moltiplicatore è possibile visualizzare unità di misura diverse negli ordini fornitore, qualora si dovessero trattare quantità da convertire per la vendita al dettaglio.

{% hint style="info" %}
E' possibile aggiungere nuove unità di misura oltre a quelle previste dal gestionale in **Strumenti/Tabelle/Unità di misura**.
{% endhint %}

Esempio: Nel caso di attività che acquistano al kg e rivendono al grammo, si dovrà impostare come unità di misura primaria il g e secondaria il kg, con relativo fattore moltiplicativo.

<figure><img src="../../../../.gitbook/assets/immagine (683).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
Per poter impostare fattori moltiplicativi con più di 2 decimali, si deve andare in **Strumenti/Impostazioni/Generali** e alla voce **Cifre decimali per quantità**, impostare il numero di decimali necessario.
{% endhint %}

In questo modo, inserendo tale articolo in un ordine fornitore con quantità pari a 2000g, sulla stampa del documento la quantità risulterà invece pari a 2kg, avendo effettuato la conversione.

Esempio 2: Nel caso di acquisto di licenze mensili e rivendita annualmente, si dovrà impostare come unità di misura primaria il mese e secondaria l'anno, con relativo fattore moltiplicativo.

<figure><img src="../../../../.gitbook/assets/immagine (578).png" alt=""><figcaption></figcaption></figure>

In questo modo, inserendo tale articolo in un ordine fornitore con quantità pari a 12 mesi, sulla stampa del documento la quantità risulterà invece pari a 1 anno, avendo effettuato la conversione.

Esempio 3: Nel caso di acquisto di licenze annuali da rivendere mensilmente, si dovrà impostare come unità di misura primaria l'anno e secondaria il mese, con relativo fattore moltiplicativo.

<figure><img src="../../../../.gitbook/assets/immagine (889).png" alt=""><figcaption></figcaption></figure>

In questo modo, inserendo tale articolo in un ordine fornitore con quantità pari a 1 anno, sulla stampa del documento la quantità risulterà invece pari a 12 mesi, avendo effettuato la conversione.

### Vendita

* Coefficiente di vendita
* Prezzo di vendita
* Minimo di vendita
* Iva di vendita
* Conto predefinito di vendita

<figure><img src="../../../../.gitbook/assets/immagine (69).png" alt=""><figcaption></figcaption></figure>

E' inoltre possibile visualizzare nella schermata sottostante gli ultimi 20 prezzi di acquisto e di vendita dell'articolo, e caricare eventuali allegati.

## Plugin

Selezionando uno specifico record si può accedere a diversi plugin nella barra laterale della pagina:

* Movimenti
* Serial
* Giacenze
* Statistiche
* Netto clienti
* Listino fornitori
* Piani di sconto/magg.
* Varianti Articolo
* Provvigioni
* Barcode
* Note interne
* Info

## Informazioni aggiuntive

{% content-ref url="azioni-aggiuntive.md" %}
[azioni-aggiuntive.md](azioni-aggiuntive.md)
{% endcontent-ref %}

{% content-ref url="plugin/" %}
[plugin](plugin/)
{% endcontent-ref %}

{% content-ref url="../../strumenti/import/import-articoli.md" %}
[import-articoli.md](../../strumenti/import/import-articoli.md)
{% endcontent-ref %}

{% content-ref url="../../../../guide/esempi/prezzo-di-vendita-automatico.md" %}
[prezzo-di-vendita-automatico.md](../../../../guide/esempi/prezzo-di-vendita-automatico.md)
{% endcontent-ref %}
