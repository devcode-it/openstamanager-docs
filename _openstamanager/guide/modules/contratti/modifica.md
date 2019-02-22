---
title: Modifica contratto
add:
  - path: add-1.png
    alt: Aggiunta articolo
    title: Schermata di aggiunta articolo
  - path: add-2.png
    alt: Aggiunta descrizione
    title: Schermata di aggiunta descrizione
change:
  - path: edit-row.png
    alt: Modifica riga
    title: Schermata di modifica riga
  - path: rows-3.png
    alt: Articoli e righe
    title: Screenshot della gestione di articoli e righe
---

# modifica

La sezione di modifica degli elementi del modulo segue il sistema standard del gestionale, necessitando il click sulla riga relativa al _record_ all'interno della tabella della schermata principale.

## Caratteristiche

La sezione di modifica del modulo **Contratti** permette di procedere alla modifica dei seguenti campi di base:

* Numero
* Nome
* Cliente
* Sede
* Agente
* Referente
* Rinnovabile
* Preavviso per il rinnovo \(in giorni\)
* Validità \(in giorni\)
* Metodo di pagamento
* Date di bozza, accettazione, conclusione e rifiuto
* Stato
* Impianti interessati
* Esclusioni
* Descrizione

E' inoltre supportata la gestione automatica dello _Sconto incondizionato_ globale sul contratto.

### Righe

Il modulo **Contratti** integra all'interno della sezione **Righe** la gestione delle spese relative ai propri elementi.

Cliccando sui pulsanti relativi, è possibile procedere quindi alla creazione di nuove spese relative al contratto:

* Articoli
* Righe \(spese generiche\)
* Descrizioni \(righe dedicate alla stampa\)

Una volta inserite correttamente le informazioni richieste, la nuova spesa verrà aggiunta all'elenco del contratto.

E' quindi possibile procedere alla modifica e all'eventuale rimozione della spesa attraverso i pulsanti dedicati della spesa.

## Opzioni

Nella parte superiore della pagina viene inoltre permessa la visualizzazione di una serie di opzioni dedicate al modulo **Contratti**:

* Stampa del contratto
* Invio del contratto via email
* Possibilità di creare una fattura dal contratto
* Possibilità di [rinnovare il contratto](modifica.md#rinnova)

### Rinnova

La funzionalità _Rinnova_ viene resa disponibile se il campo _Rinnovabile_ del contratto viene selezionato. In questo caso, una volta definite le date di accettazione e conclusione \(_Data accettazione_ e _Data conclusione_\), sarà possibile sfruttare questa opzione per copiare il contratto con le rispettive date traslate di conseguenza a partire dal giorno successivo alla _Data conclusione_.

La procedura di rinnovazione replica in modo completo le spese relative al contratto e le pianificazioni relative, rimuovendo però gli interventi che erano stato collegati in precedenza \(che, logicamente, rimarranno in relazione con il contratto precedente\).

## Particolarità

La creazione di righe con unità di misura _ore_ viene sfruttata dal plugin **Consuntivo** per monitorare l'utilizzo delle stesse all'interno delle attività collegate.

