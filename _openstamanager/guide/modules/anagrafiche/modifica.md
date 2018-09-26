---
title: Modifica anagrafica
---

La sezione di modifica degli elementi del modulo segue il sistema standard del gestionale, necessitando il click sulla riga relativa al *record* all'interno della tabella della schermata principale.

## Caratteristiche

Una volta all'interno di questa parte del sistema, il modulo **Anagrafiche** permette di completare *tutte* le informazioni che il gestionale supporta per le anagrafiche.
In particolare, per permettere un maggiore senso logico nella navigazione dei dati, la sezione di modifica è suddivisa in 3 raggruppamenti.

### Dati anagrafici

Il primo raggruppamento di informazioni sull'anagrafica consiste nell'insieme dei dati anagrafici relativi.

{% include figure path="section-1.png" alt="Dati anagrafici" caption="Screenshot della sezione dei dati anagrafici" %}

Attraverso questa sezione, è possibile procedere alla modifica delle informazioni di base dell'anagrafica in questione:
 - Ragione sociale
 - Tipologia (Azienda/Privato/Ente pubblico)
 - Informazioni sulla nascita (o fondazione)
 - Sesso
 - Codice interno dell'anagrafica
 - Indirizzo PEC
 - Sito web


### Sede legate

Viene quindi presentata una selezione di campi relativi alle informazioni sulla *sede legale* dell'anagrafica, quali:
 - Partita IVA
 - Codice fiscale
 - Informazioni varie sulla sede (per maggiori informazioni, visitare la sezione [Sedi](sedi.md))

{% include figure path="section-2.png" alt="Sede legale" caption="Screenshot della sezione sulla sede legale" %}

In particolare, se l'impostazione **Google Maps API key** viene impostata, sarà possibile visualizzare attraverso Google Maps l'indirizzo indicato ed eventualmente definire manualmente longitudine e latitudine.

### Informazioni aggiuntive

L'ultimo raggruppamento di informazioni presenta una serie di elementi non fondamentali per ogni tipologia di anagrafica, ma che potrebbero essere utili in base alle necessità dell'utente (tra cui la possibilità di cambiare la tipologia dell'anagrafica) .

{% include figure path="section-3.png" alt="Informazioni aggiuntive" caption="Screenshot della sezione di informazioni aggiuntive" %}

## Altro

In alcuni casi, l'eliminazione dell'anagrafica viene impedita.

Questa condizione si verifica quando esiste un collegamento interno dell'elemento con altre componenti del gestionale.

{% include figure path="info.png" alt="Info" caption="Screenshot della informazioni di eliminazione" %}

## Fatturazione Elettronica

Il sistema integrato di Fatturazione Elettronica per la generazione dei file XML relativi richiede la compilazione obbligatoria di una serie di campi.

Informazioni da completare.
{: .notice--warning}
