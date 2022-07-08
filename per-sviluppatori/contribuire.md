---
title: Contribuire
sidebar:
  nav: docs-sidebar
description: Come contribuire allo sviluppo di OpenSTAManager
---

# 📒 Contribuire

Sei interessato a contribuire allo sviluppo di OpenSTAManger? Ottimo, sei il benvenuto!

Siamo entusiasti di ogni contributo che otteniamo dalla nostra community. Ci sono molti modi per contribuire: segnalare bug, richiedere miglioramenti, richiedere guide, proporre fix, ecc

Non serve essere degli esperti programmatori per aiutarci!

Leggi le seguenti sezioni per scoprire come ti consigliamo di procedere. Se ti serve un aiuto, crea una issue su GitHub.

#### Linee guida

Per migliorare il sistema con cui sviluppiamo il codice, abbiamo deciso di adottare alcune linee guida per facilitare la collaborazione:

* Codice di condotta: Per il momento non abbiamo adottato un vero e proprio codice di condotta, ma ti chiediamo di essere il più civile possibile nel comunicare con gli altri per questo progetto.
* Stile del codice: Utilizziamo principalmente due strumenti per mantenere consistente nel tempo lo stile del codice:
  * [PHP CS Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer)
  * [EditorConfig](http://editorconfig.org)

PHP CS Fixer viene utilizzato per formattare automaticamente il codice PHP e aumentare la sua comprensibilità. La configurazione può essere trovata nel file [.php\_cs](https://github.com/devcode-it/openstamanager/blob/master/.php\_cs).

EditorConfig viene sfruttato per mantenere la consistenza nella formattazione di base dei diversi altri file utilizzati nel progetto. La configurazione può essere trovata nel file [.editorconfig](https://github.com/devcode-it/openstamanager/blob/master/.editorconfig).

Maggiori informazioni sui plugin che permettono di integrare questi strumenti sono disponibili nei relativi siti.

### 🔖 Prima contribuzione

Sei insicuro su cosa potresti lavorare per contribuire al progetto?

Prova a dare un'occhiata alle issue sotto la label [nuovi contributori](https://github.com/devcode-it/openstamanager/labels/nuovi%20contributori), dove sono indicate le migliorie più semplici da applicare.

### 🔖 Problemi di sicurezza

{% hint style="danger" %}
Se trovi un problema di sicurezza, NON aprire una issue.

Inviaci un'email all'indirizzo `info@openstamanager.com`
{% endhint %}

Per capire se hai individuato un problema di sicurezza, prova a farti queste domande:

* Posso accedere a qualcosa a cui non dovrei avere accesso?
* Posso disabilitare qualcosa per altre persone?

Se la risposta a una di queste domande è positiva, allora probabilmente hai individuato un problema di sicurezza. Considera però che anche in caso negativo potrebbe trattarsi di un problema di questo tipo, quindi se sei insicuro contattaci comunque via email.

### 🔖 Segnalare un bug

Se hai individuato un bug e desideri segnalarlo, apri una nuova issue provando a mantenerti sulla base del [file di template su GitHub](https://github.com/devcode-it/openstamanager/blob/master/.github/ISSUE\_TEMPLATE.md).

Se vuoi suggerire una miglioria o una nuova funzionalità, sentiti libero di aprire una issue apposita dove spieghi dettagliatamente la modifica che vorresti, la sua utilità e il suo funzionamento generale, e valuteremo la tua richiesta.

### 🔖 Pull Request

Se sei in grado di risolvere uno dei bug segnalati oppure vuoi completare una nuova funzionalità, apri una nuova Pull Request provando a mantenerti sulla base del [file di template su GitHub](https://github.com/devcode-it/openstamanager/blob/master/.github/PULL\_REQUEST\_TEMPLATE.md).

## 🫂Community

Siamo presenti su:

* [Facebook](https://www.facebook.com/openstamanager)
* [Forum](https://forum.openstamanager.com/)
* [Instagram](https://www.instagram.com/openstamanager)
* [Twitter](https://www.twitter.com/openstamanager)
* [Youtube](https://www.youtube.com/channel/UCoToaK4dhDXmcQXi1AnqQ4Q)

## 🏗️ Testing

Il progetto presenta, a partire dalla versione 2.4.2, un insieme di test per facilitare il controllo sul corretto funzionamento del gestionale.

Per eseguire i test è necessario seguire le seguenti istruzioni ([https://codeception.com/docs/modules/WebDriver](https://codeception.com/docs/modules/WebDriver)):

* Scaricare (Selenium Server)\[[https://docs.seleniumhq.org/download/](https://docs.seleniumhq.org/download/)] e salvarlo come `selenium-server-standalone.jar` nella cartella principale
* Scaricare (ChromeDriver)\[[https://sites.google.com/a/chromium.org/chromedriver/getting-started](https://sites.google.com/a/chromium.org/chromedriver/getting-started)], rendendolo eseguibile da riga di comando (su Windows, aggiungerlo al PATH)
* Configurare localmente Codeception nel file `codeception.yml` con l'URL del web server locale
*   Eseguire su shell differenti i seguenti comandi:

    ```bash
    npm run tests-server    # Avvia i server per i test di funzionamento grafico
    npm run tests-OSM       # Avvia i test
    ```
