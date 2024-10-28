---
description: Guida alla struttura di OpenSTAManager
---

# 📒 Nucleo

Scaricando la versione GIT del progetto dovreste trovare una struttura di base molto simile a quella seguente.

```
.
├── api
├── assets
├── backup
├── config
├── files
├── include
├── lib
├── locale
├── logs
├── modules
├── node_modules
├── plugins
├── src
├── templates
├── tests
├── update
└── vendor
```

Analizzeremo ora in dettaglio la funzione delle diverse cartelle e dei relativi contenuti. Si avverte che il gestionale è fortemente basato sulla correttezza contemporanea di molti file: siete pertanto pregati di astenervi da modifiche o, se queste dovessero rivelarsi necessarie, procedere alla creazione di un relativo file custom nella cartella del file. E' comunque consigliabile richiedere l'assistenza ufficiale.

{% hint style="info" %}
Per maggiori informazioni riguardanti la procedura di personalizzazione, rivolgersi alle specifiche sezioni di ogni settore.
{% endhint %}

## 📒 Root

I contenuti della cartella _root_ sono estremamente importanti per il progetto, in quanto sono generalmente dedicati a garantire il corretto funzionamento dell'intero gestionale. Questa centralizzazione permette al software di essere estremamente scalabile e personalizzabile, soprattutto in relazione ai moduli. Per maggiori informazioni riguardanti lo sviluppo di un modulo, consultare la sezione [Moduli](../../../openstamanager/modules/).

### 📒 add.php

Il file `add.php` è dedicato alla gestione dei form di creazione nuovi elementi all'interno dei vari moduli.

In particolare si occupa parallelamente della funzionalità di aggiunta al volo, visibile in azione nei modulo **Attività**, **Articoli** e in alcuni altri punti del software.

### 📒 ajax\_complete.php

Il file `ajax_dataload.php` gestisce il caricamento dinamico dei dati in varie sezioni del sito, relativamente alle operazioni di auto-completamento dei form e della ricerca globale.

**Attenzione**: questo sistema è ormai deprecato e, tranne in rari casi, completamente sostituito dall'utilizzo del file `ajax_select.php` e dal plugin [Select2](https://select2.github.io).

### 📒 ajax\_dataload.php

Il file `ajax_dataload.php` gestisce il caricamento dinamico dei dati nelle tabelle fornite nella vista generale dei moduli (`controller.php`), filtrando i risultati in base alle richieste dell'utente.

### 📒 ajax\_select.php

Il file `ajax_select.php` gestisce il caricamento dinamico dei dati nei diversi select abilitati, garantendo l'accesso a tutti i _record_ senza provocare rallentamenti (persino per numeri più elevati).

### 📒 bug.php

Il file `bug.php` si occupa della segnalazione dei bug, fornendo un sistema integrato di invio email dopo la configurazione di pochi parametri iniziali.

Le opzioni relative alle informazioni da allegare sono:

* Allegare il file di log (fondamentale nel caso si stia effettuando una segnalazione)
* Allegare una copia del database
* Allegare le informazioni relative al PC utilizzato

### 📒 core.php

Il _core_ contiene il nucleo dell'intero gestionale: si occupa delle operazioni di inizializzazione fondamentali, compresa l'inclusione del file di configurazione `config.inc.php` e la creazione dell'elenco degli assets da includere. Si occupa inoltre del controllo dei permessi, tramite il richiamo alla specifica classe `Permissions`, e dell'individuazione delle informazioni di base relative al modulo in utilizzo.

### 📒 config.inc.php

Il file `config.inc.php` contiene tutte le informazioni per accedere correttamente al database e per determinare il tema utilizzato dal gestionale.

**Attenzione**: questo file non è presente di default poiché obbligatoriamente da personalizzare tramite la procedura di installazione. La struttura di base può essere comunque osservata all'interno del file `config.example.php`. {: .notice--danger}

### 📒 controller.php

Il file `controller.php` si occupa di gestire l'accesso generico ai moduli, caricando le informazioni e i widget del modulo in oggetto. Permette inoltre la visualizzazione, in base ai permessi accordati all'utente, del pulsante di creazione nuovi elementi.

### 📒 editor.php

Il file `editor.php` si occupa di gestire l'accesso specifico ai dati di un singolo elemento di un modulo, caricando al tempo stesso l'insieme di plugin (e, in casi più rari, di widget) legati alla visualizzazione dell'elemento in oggetto. Permette inoltre, in base ai permessi accordati all'utente, la modifica dei dati inseriti e l'interazione con altri moduli.

### 📒 index.php

Il file `index.php` si occupa delle operazioni di accesso e scollegamento al gestionale, oltre che effettuare un controllo sulla disponibilità di aggiornamenti (tramite l'inclusione di `include/update.php`) e a garantire il redirect iniziale al primo modulo su cui l'utente possiede i permessi di accesso.

### 📒 info.php

Il file `info.php` contiene la sezione informativa relativa al progetto, indicante la community, la modalità di supporto e le offerte a pagamento.

### 📒 log.php

Il file `log.php` permette di visualizzare le informazioni relative agli ultimi 100 tentativi di accesso.

{% hint style="warning" %}
**Attenzione**: nel caso in cui l'utente sia un amministratore, le informazioni accessibili sono relative a **tutti** gli utenti (al contrario, un utente normale può visualizzare esclusivamente i propri tentativi).
{% endhint %}

### 📒 composer.json, gulpfile.js, package.json

Per maggiori informazioni questi file, consultare le sezioni [Framework ](../../base/framework.md)e [Assets](../../base/assets.md).

## 📒 Cartella api

Per maggiori informazioni riguardanti la cartella `api` e i suoi contenuti, rivolgersi alla sezione [API](../../../configurazioni/introduzione.md).

## 📒 Cartella assets

Per maggiori informazioni riguardanti la cartella `assets` e i suoi contenuti, rivolgersi alla sezione [Assets](../../base/assets.md).

## 📒 Cartella backup

La cartella _backup_ è quella di default utilizzata dall'operazione omonima del progetto.

## 📒 Cartella docs

La cartella `docs`, come si può intuire, contiene la documentazione di sviluppo del progetto.

## 📒 Cartella files

Per maggiori informazioni riguardanti la cartella `files` e i suoi contenuti, rivolgersi alla sezione [Moduli](../../../openstamanager/modules/).

## 📒 Cartella include

### 📒 bottom.php

Il file `bottom.php` si occupa delle operazioni di chiusura della pagina HTML, garantendo inoltre l'eliminazione dei log temporanei della sessione.

Si ricorda che è possibile creare una personalizzazione di questa pagina nella cartella `custom`.

### 📒 top.php

Il file `top.php` gestisce la creazione del layout di base del gestionale, comprendente la barra di navigazione e la sidebar.

Si ricorda che è possibile creare una personalizzazione di questa pagina nella cartella `custom`.

## 📒 Cartella lib

La cartella `lib` contiene le librerie personalizzate e le funzioni utilizzate dall'intero gestionale nei diversi moduli.

{% hint style="warning" %}
**Attenzione**: sono qui presenti solo i metodi generali e comunemente riutilizzati. Per maggiori informazioni riguardanti la locazione delle funzioni specifiche di un modulo, visitare la sezione [Moduli](../../../openstamanager/modules/).
{% endhint %}

### 📒 deprecated.php

Il file `deprecated.php` contiente l'insieme di funzioni deprecate nella versione corrente del gestionale, che verranno successivamente rimosse nella futura release.

### 📒 functions.php

Il file `functions.php` contiene tutte le funzioni comunemente utilizzate nel progetto.

### 📒 functionsjs.php

Il file `functionsjs.php` contiene tutte le funzioni JavaScript comunemente utilizzate nel progetto.

### 📒 init.js

Il file `init.js` contiene le funzioni JavaScript comunemente richiamate al caricamento di parti indipendenti del progetto.

## 📒 Cartella locale

La cartella `locale` contiene tutte le traduzioni del progetto, nei formati tipici di Gettext (`.po` e `.mo`).

## 📒 Cartella modules

Per maggiori informazioni riguardanti la cartella `modules` e i suoi contenuti, rivolgersi alla sezione [Moduli](../../../openstamanager/modules/). Si ricorda che per tutti i contenuti del modulo è possibile creare una personalizzazione nella cartella `custom`.

## 📒 Cartella templates

La cartella `templates` contiene tutti i file relativi alla visualizzazione in PDF dei dati dei vari moduli. Per maggiori informazioni riguardanti la cartella `templates` e i suoi contenuti, rivolgersi alla sezione [Stampe](stampe.md).

## 📒 Cartella update

### 📒 create\_updates.sql

Il file `create_updates.sql` contiene la query SQL per la creazione della tabella di gestione degli aggiornamenti e delle installazioni del gestionale.

### 📒 VERSIONE.sql

I file `VERSIONE.sql` contengono l'insieme di query SQL necessarie per l'aggiornamento del gestionale alla versione _VERSIONE_.

### 📒 VERSIONE.php

I file `VERSIONE.php` contengono l'insieme di operazioni PHP (e, talvolta, SQL) necessarie per l'aggiornamento del gestionale alla versione _VERSIONE_.

## 📒 Cartella vendor

{% hint style="info" %}
Per maggiori informazioni riguardanti la cartella `vendor` e i suoi contenuti, rivolgersi alla sezione [Framework](../../base/framework.md).
{% endhint %}
