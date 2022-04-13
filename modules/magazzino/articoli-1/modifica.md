---
title: Modifica articolo
---

# Modifica

La sezione di modifica degli elementi del modulo segue il sistema standard del gestionale, necessitando il click sulla riga relativa al _record_ all'interno della tabella della schermata principale.

## Caratteristiche

Una volta all'interno di questa parte del sistema, il modulo **Articolo** permette di completare _tutte_ le informazioni che il gestionale supporta per l' articolo. In particolare, per permettere un maggiore senso logico nella navigazione dei dati, la sezione di modifica è suddivisa in 3 raggruppamenti:

* [Dati dell'articolo](modifica.md#dati-dellarticolo)
* Giacenze totale
* [Dati di acquisto e vendita](modifica.md#dati-di-acquisto-e-vendita)
* [Componenti](modifica.md#componenti)
* [Listini](modifica.md#listini)

### Dati dell'articolo

Il primo raggruppamento di informazioni sull'articolo consiste nell'insieme delle informazioni basilari relative.

In particolare, attraverso questa sezione è possibile procedere alla modifica dei seguenti campi:

* Immagine
* Codice
* Barcode
* Categoria
* Sottocategoria
* Descrizione (dal _Nome_ richiesto nella creazione)
* Ubicazione
* Unità di misura predefinita
* Note eventuali

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2F3ClG0vK4TyrPjkS7xtBH%2Ffile.png?alt=media)

Vengono rese inoltre disponibili alcune altre opzioni estremamente importanti per la gestione interna dell'articolo:

* _**Abilita serial number**_ \_\*\*\_permette l'abilitazione della gestione dei numeri seriali per l'articolo
* _**Seleziona per rendere attivo l'articolo**_ permette, se disabilitato, di impedire l'utilizzo dell'articolo

### Giacenze totale

Il secondo raggruppamento di informazioni sull'articolo consiste nell'insieme delle informazioni di magazzino relative.

Attraverso questa sezione è possibile procedere alla visualizzazione della quantità a magazzino e alla modifica della stessa effettuando un movimento di magazzino manuale.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2Fxdi8xIt7PznlKPcM1gfC%2Ffile.png?alt=media)

### Dati di acquisto e vendita

Viene quindi presentata una selezione di campi relativi alle informazioni di acquisto e vendita relative all'articolo, suddivise rispettivamente nelle sezioni **Acquisto** e **Vendita**.

La componente **Acquisto** permette il completamento delle informazioni di:

* _Prezzo di acquisto_
* _Soglia minima quantità(per il widget **Articoli in esaurimento** nel modulo **Dashboard)**_
* _Fornitore predefinito (è possibile selezionare i fornitori a cui è stato inserito un prezzo nel plugin **Prezzi specifici**)_
* _Conto predefinito_
* _Unità di misura secondaria (per le stampe ordini fornitori)_
* _Fattore moltiplicativo (per le stampe ordini fornitori)_
* _Quantità multipla (scorta minima dell'articolo a magazzino, è un campo di informazione non propone l'ordine al fornitore)_

La sezione **Vendita** presenta i seguenti campi:

* _Prezzo_
* _Iva predefinita_
* _Conto predefinito_
* _Garanzia_ (in giorni)
* _Volume_ (in m^3)
* _Peso lordo_ (in KG)
* _Questo articolo è un servizio_ (disabilita la modifica della quantità per l'articolo)

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FZkKiXybhdwLnzrZ8I9hY%2Ffile.png?alt=media)

### Componenti

Il raggruppamento **Componenti** permette di gestire gli elementi del modulo **Gestione componenti** (sotto **Impianti**) collegati all'articolo.

### Listini

L'ultimo raggruppamento di informazioni presenta la previsione di rincaro/sconto relativa ad ogni listino registrato nel modulo **Listini**, permettendo in questo modo il calcolo automatico del prezzo effettivo in base al listino collegato all'anagrafica.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2F5qFx2GIGJWn2KeW46Xo8%2Ffile.png?alt=media)

## Particolarità

{% hint style="info" %}
L'immagine dell'articolo viene considerata a tutti gli effetti come un upload tradizionale.
{% endhint %}
