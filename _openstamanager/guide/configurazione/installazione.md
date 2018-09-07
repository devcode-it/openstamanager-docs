---
title: Installazione
requirements:
  - path: requirements-error.png
    alt: "Schermata dei requisiti (non soddisfatti)"
    title: "Requisiti non soddisfatti"
  - path: requirements-ok.png
    alt: "Schermata dei requisiti (soddisfatti)"
    title: "Requisiti soddisfatti"
license:
  - path: license.png
    alt: "Schermata per la licenze"
    title: "Licenza"
  - path: license-error.png
    alt: "Errore di licenza"
    title: "Licenza non accettata"
test:
  - path: config-test.png
    alt: "Test della configurazione"
    title: "Test"
  - path: config-ok.png
    alt: "Test ok"
    title: "Successo del test"
  - path: config-error.png
    alt: "Test error"
    title: "Errore di test"
error:
  - path: connection-error.png
    alt: "Errore di connessione"
    title: "Errore di connessione"
  - path: write-error.png
    alt: "Errore di scrittura"
    title: "Errore di scrittura"
install:
  - path: install.png
    alt: "Installazione del database"
    title: "Installazione del database"
  - path: installing.png
    alt: "Processo di installazione del database"
    title: "Processo di installazione del database"
  - path: installed.png
    alt: "Database installato con successo"
    title: "Database installato con successo"
---

Per procedere all'installazione di OpenSTAManager è necessario seguire i seguenti punti:

1. [Scaricare una release ufficiale del progetto](https://github.com/devcode-it/openstamanager/releases).
2. Creare una cartella (ad esempio `openstamanager`) nella root del *web server* ed estrarvi il contenuto della release scaricata (per maggiori informazioni, [consultare la documentazione tecnica](../../docs/installazione.md))
3. Creare un database vuoto (tramite [PHPMyAdmin](http://localhost/phpmyadmin/) o riga di comando).
4. Accedere a <http://localhost/openstamanager> dal vostro browser.

Una volta completate le istruzioni per l'installazione del software, è necessario procedere alla sua configurazione per permetterne il funzionamento nell'ambiente di utilizzo.

Questa procedura può essere suddivisa in tre sezioni differenti:
 - Controllo dei requisiti
 - Revisione della licenza del software
 - Configurazione delle credenziali di accesso al database MySQL

## Requisiti

Il software permette in automatico di controllare se l'ambiente di utilizzo presenta una configurazione adeguata per il suo corretto funzionamento.

In particolare, viene richiesta la presenza di un *web server* [Apache](https://httpd.apache.org/) con il linguaggio di programmazione [PHP](http://php.net) e il [DBMS MySQL](https://www.mysql.com), richiedendo le seguenti versioni minime:

- PHP >= 5.6
- MySQL >= 5.6.5

Nel caso la versione PHP non sia compatibile, viene mostrato immediatamente un messaggio informativo a riguardo:
{% include figure path="basic.png" alt="Controllo sui requisiti PHP" caption="Requisto PHP non soddisfatto" %}

Successivamente, se il controllo precedente viene soddisfatto, il software verrà effettivamente avviato e sarà possibile procedere nella configurazione.

Viene quindi caricata la pagina per il controllo della configurazione del *web server*, di cui vengono controllati vari componenti:
 - Moduli Apache
 - Estensioni PHP
 - Percorsi di servizio per il software

{% include gallery id="requirements" caption="Requisiti interni del software" %}

Nel caso vengano mostrati dei componenti in rosso, è consigliato procedere all'attivazione del modulo/estensione seguendo le linee guida ufficiali del relativi software ([PHP]() o [Apache](https://stackoverflow.com/a/5758551)).

Una volta corretti correttamente i requisiti, cliccare su **Successivo**.

## Licenza

La scheramata successiva a quella dei requisiti consiste nella gestione della licenza di utilizzo del software.

OpenSTAManager viene reso disponibile tramite una licenza **GPL-3.0**, che ne permette l'uso commerciale e la personalizzazione a patto di mantenere un riferimento al progetto iniziale rimuovendo la resposabilità di eventuali problematiche agli sviluppatori originali.

**Non è possibile procedere all'utilizzo del software senza aver accettato la licenza.**

{% include gallery id="license" caption="Licenza del software" %}

Una volta accettata la licenza, cliccare su **Successivo**.

## Database

Una volta corretti i requisiti e accettata la licenza, viene resa disponibile la pagina dedicata alla configurazione del software per l'accesso al databas MySQL.

{% include figure path="config.png" alt="Pagina di configurazione" caption="Screenshot delle pagina di configurazione" %}

E' possibile, una volta completate le informazioni di configurazione, procedere ad un test automatico per controllare se il database presente è completamente compatibile con il gestionale.
Questa funzione è disponibile attraverso il pulsante **Testa il database**.

{% include gallery id="test" caption="Possibilità di test della configurazione" %}

In ogni caso, si possono verificare degli errori duranti il salvataggio della configurazione se:
 - I dati di connessione sono errati
 - I permessi di creazione e scrittura sul file `config.inc.php` sono troppo restrittivi

{% include gallery id="error" caption="Errori nel salvataggio della configurazione" %}

Se le credenziali inserite sono corrette, dopo aver cliccato su **Installa** si verrà reindirizzati alla procedura automatica di installazione del database.

## Installazione del database

Una volta inseriti correttamente i parametri di configurazione, è sufficiente cliccare sul pulsante **Installa!** per avviare l'installazione del database di OpenSTAManager.
{% include gallery id="install" caption="Procedura di installazione del database" %}

Per maggiori informazioni su questa procedura, oppure nel caso si verificassero degli errori, visitare la sezione **Aggiornamento**.

[Vai alla sezione Aggiornamento](aggiornamento.md){: .btn .btn--info .btn--x-large .btn--block}

## Inizializzazione

Una volta completati i precedenti passaggi con successo, verrà richiesta di inizializzare il gestionale con delle informazioni di base.

[Vai alla sezione Inizializzazione](inizializzazione.md){: .btn .btn--success .btn--x-large .btn--block}
