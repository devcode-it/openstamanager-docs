---
title: Modifica contratto
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

La sezione di modifica del modulo **Contratti** permette di procedere alla modifica dei seguenti campi di base:
 - Numero
 - Nome
 - Cliente
 - Sede
 - Agente
 - Referente
 - Rinnovabile
 - Preavviso per il rinnovo (in giorni)
 - Validità (in giorni)
 - Metodo di pagamento
 - Date di bozza, accettazione, conclusione e rifiuto
 - Stato
 - Impianti interessati
 - Esclusioni
 - Descrizione

E' inoltre supportata la gestione automatica dello *Sconto incondizionato* globale sul contratto.

{% include figure path="section-1.png" alt="Dati del contratto" caption="Screenshot dei dati del contratto" %}

### Righe

Il modulo **Contratti** integra all'interno della sezione **Righe** la gestione delle spese relative ai propri elementi.

{% include figure path="rows-1.png" alt="Articoli e righe" caption="Screenshot della gestione di articoli e righe" %}

Cliccando sui pulsanti relativi, è possibile procedere quindi alla creazione di nuove spese relative al contratto:
 - Articoli
 - Righe (spese generiche)
 - Descrizioni (righe dedicate alla stampa)

{% include figure path="add-row.png" alt="Aggiunta riga" caption="Screenshot della sezione di aggiunta di una riga" %}

{% include gallery id="add" caption="Schermate di aggiunta spese" %}

Una volta inserite correttamente le informazioni richieste, la nuova spesa verrà aggiunta all'elenco del contratto.

{% include figure path="rows-2.png" alt="Articoli e righe" caption="Screenshot della gestione di articoli e righe" %}

E' quindi possibile procedere alla modifica e all'eventuale rimozione della spesa attraverso i pulsanti dedicati della spesa.

{% include gallery id="change" caption="Schermate di modifica spese" %}

## Opzioni

Nella parte superiore della pagina viene inoltre permessa la visualizzazione di una serie di opzioni dedicate al modulo **Contratti**:
 - Stampa del contratto
 - Invio del contratto via email
 - Possibilità di creare una fattura dal contratto
 - Possibilità di [rinnovare il contratto](#rinnova)

{% include figure path="options.png" alt="Opzioni" caption="Screenshot della opzioni dell'attività" %}

### Rinnova

La funzionalità *Rinnova* viene resa disponibile se il campo *Rinnovabile* del contratto viene selezionato.
In questo caso, una volta definite le date di accettazione e conclusione (*Data accettazione* e *Data conclusione*), sarà possibile sfruttare questa opzione per copiare il contratto con le rispettive date traslate di conseguenza a partire dal giorno successivo alla *Data conclusione*.

La procedura di rinnovazione replica in modo completo le spese relative al contratto e le pianificazioni relative, rimuovendo però gli interventi che erano stato collegati in precedenza (che, logicamente, rimarranno in relazione con il contratto precedente).

## Particolarità

La creazione di righe con unità di misura *ore* viene sfruttata dal plugin **Consuntivo** per monitorare l'utilizzo delle stesse all'interno delle attività collegate.

{% include figure path="consuntivo.png" alt="Plugin Consuntivo" caption="Screenshot del plugin **Consuntivo**" %}
