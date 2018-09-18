---
title: Modifica preventivo
add:
  - path: add-1.png
    alt: "Aggiunta articolo"
    title: "Schermata di aggiunta articolo"
  - path: add-2.png
    alt: "Aggiunta descrizione"
    title: "Schermata di aggiunta descrizione"
change:
  - path: edit-row.png
    alt: "Modifica riga"
    title: "Schermata di modifica riga"
  - path: rows-3.png
    alt: "Articoli e righe"
    title: "Screenshot della gestione di articoli e righe"
---

La sezione di modifica degli elementi del modulo segue il sistema standard del gestionale, necessitando il click sulla riga relativa al *record* all'interno della tabella della schermata principale.

## Caratteristiche

La sezione di modifica del modulo **Preventivi** permette di procedere alla modifica dei seguenti campi di base:
 - Numero
 - Nome
 - Cliente
 - Agente
 - Referente
 - Tempi di consegna
 - Validità (in giorni)
 - Metodo di pagamento
 - Date di bozza, accettazione, conclusione e rifiuto
 - Stato
 - Tipo di attività
 - Esclusioni
 - Descrizione

E' inoltre supportata la gestione automatica dello *Sconto incondizionato* globale sul preventivo.

{% include figure path="section-1.png" alt="Dati del preventivo" caption="Screenshot dei dati del preventivo" %}

### Righe

Il modulo **Preventivi** integra all'interno della sezione **Righe** la gestione delle spese relative ai propri elementi.

{% include figure path="rows-1.png" alt="Articoli e righe" caption="Screenshot della gestione di articoli e righe" %}

Cliccando sui pulsanti relativi, è possibile procedere quindi alla creazione di nuove spese relative al preventivo:
 - Articoli
 - Righe (spese generiche)
 - Descrizioni (righe dedicate alla stampa)

{% include figure path="add-row.png" alt="Aggiunta riga" caption="Screenshot della sezione di aggiunta di una riga" %}

{% include gallery id="add" caption="Schermate di aggiunta spese" %}

Una volta inserite correttamente le informazioni richieste, la nuova spesa verrà aggiunta all'elenco del preventivo.

{% include figure path="rows-2.png" alt="Articoli e righe" caption="Screenshot della gestione di articoli e righe" %}

E' quindi possibile procedere alla modifica e all'eventuale rimozione della spesa attraverso i pulsanti dedicati della spesa.

{% include gallery id="change" caption="Schermate di modifica spese" %}
