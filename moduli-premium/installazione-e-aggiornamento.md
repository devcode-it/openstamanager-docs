---
description: >-
  Procedura di installazione e aggiornamento per i moduli aggiuntivi di
  OpenSTAManager
---

# 📙 Installazione

OpenSTAManager presenta una struttura modulare appositamente pensata per prevedere l'installazione di moduli aggiuntivi e la personalizzazione di quelli esistenti.

### Formato del pacchetto

Al momento il gestionale supporta l'installazione diretta di due componenti tramite la [procedura semplificata](installazione-e-aggiornamento.md#procedura-semplificata) del modulo **Aggiornamenti**: moduli e plugin. Questi componenti possono essere installati e aggiornati in gruppo o singolarmente tramite un apposito archivio ZIP, che segue una struttura di base ben definita.

Ogni componente deve essere presente in una cartella separata, che deve contenere il relativo file `MODULE` oppure `PLUGIN` per permettere a OpenSTAManager di identificarlo.

```
componente.zip
├── modulo_test
|   ├── ... - File contententi il codice del modulo
|   └── MODULE
├── plugin_test
|   ├── ... - File contententi il codice del plugin
|   └── PLUGIN
└── README
```

I contenuti del file `MODULE` devono essere i seguenti:

```
directory = "Cartella di installazione"
name = "Nome del modulo"
options = "Operazione da eseguire all'apertura"
version = "Versione"
compatibility = "Versioni di compatibilità"
order = "Ordine in cui visualizzare il modulo"
default = "Se predefinito"
enabled = "Se abilitato"
icon = "Ico
parent = "Genitore del modulo"
```

I contenuti del file `PLUGIN` devono essere i seguenti:

```
directory = "Cartella di installazione"
name = "Nome del plugin"
options = "Operazione da eseguire all'apertura"
idmodule_from = "Nome del modulo di origine"
idmodule_to = "Nome del modulo di destinazione e visualizzazione"
position = "Tipo di modulo (valori disponibili: tab)"
version = "Versione"
compatibility = "Versioni di compatibilità"
order = "Ordine in cui posizionare il plugin"
enabled = "Se abilitato"
```

Alcuni esempi sulla struttura dei moduli personalizzati sono disponibili nella repository [https://github.com/devcode-it/example](https://github.com/devcode-it/example).

### Procedura semplificata

Una volta acquistato un modulo aggiuntivo e scaricato l'archivio ZIP contenente i componenti da installare o aggiornare, si può procedere con i seguenti passaggi per caricare il file nel gestionale:

* Cliccare sul modulo **Strumenti** e aprire **Aggiornamenti**

<figure><img src="../.gitbook/assets/immagine (145).png" alt=""><figcaption></figcaption></figure>

* Cliccare sul tasto ![](../.gitbook/assets/Sfoglia.png) e selezionare il file `.zip` ricevuto precedentemente.

<figure><img src="../.gitbook/assets/immagine (146).png" alt=""><figcaption></figcaption></figure>

* Cliccare sul tasto ![](../.gitbook/assets/Carica.PNG) per andare a caricare il modulo in OpenSTAManager.
* Confermare la procedura cliccando su **SI**.

<figure><img src="../.gitbook/assets/immagine (147).png" alt=""><figcaption></figcaption></figure>

* Dopo il refresh della pagina, può essere richiesto di aggiornare il database

<figure><img src="../.gitbook/assets/immagine (1303).png" alt=""><figcaption></figcaption></figure>

In seguito a questi passaggi, dovrebbe essere possibile continuare a utilizzare il gestionale normalmente e trovare di conseguenza i nuovi componenti presenti all'interno.
