---
description: >-
  Procedura di installazione e aggiornamento per i moduli esterni e a pagamento
  di OpenSTAManager
---

# 📗 Installazione

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
name = "Nome del modulo"
version = "Versione"
directory = "Cartella di installazione"
options = "Operazione da eseguire all'apertura"
compatibility = "Versioni di compatibilità"
compatibility = "Compatibilità del modulo"
parent = "Genitore del modulo"
```

I contenuti del file `PLUGIN` devono essere i seguenti:

```
name = "Nome del plugin"
version = "Versione"
directory = "Cartella di installazione"
options = "Operazione da eseguire all'apertura"
icon = "Icona (Font-Awesome)"
compatibility = "Versioni di compatibilità"
module_from = "Nome del modulo di origine"
module_to = "Nome del modulo di destinazione e visualizzazione"
position = "Tipo di modulo (valori disponibili: tab)"
```

Alcuni esempi sulla struttura dei moduli personalizzati sono disponibili nella repository [https://github.com/devcode-it/example](https://github.com/devcode-it/example).

### Procedura semplificata

Una volta in possesso dell'archivio ZIP contenetene i componenti da installare o aggiornare, si può procedere con i seguenti passaggi per caricare il file nel gestionale.

* Cliccare sul modulo **Strumenti** e aprire **Aggiornamenti**

![](../.gitbook/assets/Passaggio1\(1\).png)

* Cliccare sul tasto ![](../.gitbook/assets/Sfoglia.png) e selezionare il file `.zip` ricevuto precedentemente.

![](../.gitbook/assets/Passaggio2\(2\).png)

* Cliccare sul tasto ![](../.gitbook/assets/Carica.PNG) per andare a caricare il modulo in OpenSTAManager.

![](../.gitbook/assets/Passaggio3.png)

* Confermare la procedura cliccando su **SI**.

![](../.gitbook/assets/Passaggio4\(1\).png)

* Dopo il refresh della pagina, può essere richiesto di aggiornare il database

![](<../.gitbook/assets/image (10).png>)

In seguito a questi passaggi, dovrebbe essere possibile continuare a utilizzare il gestionale normalmente e trovare di conseguenza i nuovi componenti presenti all'interno.
