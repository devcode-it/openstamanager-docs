---
title: Modifica articolo
---

La sezione di modifica degli elementi del modulo segue il sistema standard del gestionale, necessitando il click sulla riga relativa al *record* all'interno della tabella della schermata principale.

## Caratteristiche

Una volta all'interno di questa parte del sistema, il modulo **Articolo** permette di completare *tutte* le informazioni che il gestionale supporta per gli articolo.
In particolare, per permettere un maggiore senso logico nella navigazione dei dati, la sezione di modifica è suddivisa in vari raggruppamenti.

### Dati dell'articolo

Il primo raggruppamento di informazioni sull'articolo consiste nell'insieme delle infomazioni basilari relative.

{% include figure path="section-1.png" alt="Dati dell'articolo" caption="Screenshot della sezione dei dati dell'articolo" %}

In particolare, attraverso questa sezione è possibile procedere alla modifica dei seguenti campi:
 - Immagine
 - Codice
 - Categoria
 - Sottocategoria
 - Descrizione (dal *Nome* richiesto nella creazione)
 - Unità di misura predefinita
 - Note eventuali
 - Quantità disponibile

Vengono rese inoltre disponbili alcune altre opzioni estremamente importanti per la gestione interna dell'articolo:
 - *Abilita serial number* permette l'abilitazione della gestione dei numeri seriali per l'articolo
 - *Seleziona per rendere attivo l'articolo* permette, se disabilitato, di impedire l'utilizzo dell'articolo
 - *Modifica quantità manualmente* permette la creazione di un movimento manuale

{% include figure path="more.png" alt="Movimento manuale" caption="Screenshot della sezione dedicata al movimento manuale" %}

### Dati di acquisto e vendita

Viene quindi presentata una selezione di campi relativi alle informazioni di acquisto e vendita relative all'articolo, suddivise rispettivamnete nelle sezioni **Acquisto** e **Vendita**.

{% include figure path="section-2.png" alt="Dati di acquisto e vendita" caption="Screenshot della sezione dei dati di acquisto e vendita" %}

La componente **Acquisto** permette il completamento delle informazioni di *Prezzo*, *Soglia minima quantità* (per il widget **Articoli in esaurimento** nel modulo **Dashboard**) e *Conto predefinito*.
Parallelamente, la sezione **Vendita** possiede i seguenti campi:
 - *Prezzo*
 - *Iva predefinita*
 - *Conto predefinito*
 - *Garanzia* (in giorni)
 - *Volume* (in m^3)
 - *Peso lordo* (in KG)
 - *Questo articolo è un servizio* (disabilita la modifica della quantità per l'articolo)

### Componenti

Il raggruppamento **Componenti** permette di gestire gli elementi del modulo **Gestione componenti** (sotto **MyImpianti**) collegati all'articolo.

{% include figure path="section-3.png" alt="Componenti" caption="Screenshot della sezione di componenti" %}

### Listini

L'ultimo raggruppamento di informazioni presenta la previsione di ricaro/sconto relativa ad ogni listino registrato nel modulo **Listini**, permettendo in questo modo il calcolo automatico del prezzo effettivo in base al listino collegato all'anagrafica.

{% include figure path="section-4.png" alt="Listini" caption="Screenshot della sezione dei listini" %}

## Opzioni

Nella parte superiore della pagina viene inoltre permessa la visualizzazione di una serie di opzioni dedicate al modulo **Articoli**:
 - Stampa dell'inventario
 - [Duplicazione dell'articolo](#duplica-articolo)

{% include figure path="options.png" alt="Opzioni" caption="Screenshot della opzioni dell'articolo" %}

### Duplica articolo

La funzione *Duplica articolo* permette la creazione di un articolo simile a quello corrente, con quantità, seriali e movimenti reimpostati ai valori predefiniti.

## Paricolarità

L'immagine dell'articolo viene considerata a tutti gli effetti come un upload tradizionale.
