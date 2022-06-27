---
description: Guida ai moduli e plugin di OpenSTAManager
---

# 📚 Moduli e plugin

I moduli sono la componente principale della struttura di OpenSTAManager. Sono progettati per avere una struttura facilmente personalizzabile e mantenere comportamenti indipendenti dal resto del software.

Ogni modulo del gestionale è raggiungibile attraverso il [menu laterale](./#navigazione), ma può presentare una grafica personalizzata sulla base della funzione a cui è dedicato. Esistono però alcune caratteristiche comuni che si possono individuare quasi sempre, descritte in questa pagina.

Per ottenere maggiori informazioni sul funzionamento interno e specifico di un modulo, è necessario visitare la relativa guida dedicata.

## 📌 Pagina principale

Accedendo a ogni modulo è possibile visualizzare l'elenco generale dei record salvati in esso. Cliccando su un singolo modulo si aprirà una schermata che permetterà di andare ad analizzarlo nel dettaglio e modificarlo.

La pagina principale di un modulo può essere composta da due strutture diverse: una tabella generale oppure un sistema di contenuti personalizzati.

### 📄 Tabella generale

La schermata principale che si apre entrando in un modulo è formata da una tabella che permette una serie di operazioni comuni su tutti gli elementi registrati all'interno del modulo:

* Scorrere e visualizzare (attraverso un click) i diversi record
* Selezionare diversi record attraverso le relative righe per esportarli (in formato CSV), stamparli o copiarli
* Selezionare dei record per effettuare delle azioni generali specifiche del modulo
* Filtrare i record in base a un determinato campo utilizzando i seguenti operatori:
  * != in caso si voglia ricercare un record diverso da un dato valore;
  * \= in caso si voglia ricercare uno specifico valore;
  * \> in caso si vogliano ricercare tutti i record maggiori di un determinato valore;
  * < in caso si vogliano ricercare tutti i record minori di un determinato valore.

![](<../.gitbook/assets/immagine (50).png>)

### ✏️ Contenuti personalizzati

Esistono alcuni moduli che rappresentano informazioni non compatibili al formato tabellare, come ad esempio **Dashboard** e **Statistiche**, che porteranno rispettivamente alla visualizzazione di un calendario interagibile e di un grafico personalizzabile.

### 📤 Gestione degli upload

Alcuni moduli presentano una componente generale per permettere l'inserimento di file di vario tipo all'utente finale del gestionale. Questa funzione viene spiegata in [Gestione upload](gestione-upload.md).

## 📓 Operazioni sui record

### ➕ Creazione record

I moduli che permettono la creazione di nuovi elementi presentano un pulsante apposito ![](../.gitbook/assets/Pulsante+.PNG) vicino all'intestazione della pagina.

![Pulsante di creazione record (Anagrafiche)](../.gitbook/assets/add-button.png)

Una volta cliccato il pulsante in questione, verrà aperta una schermata sovrapposta al resto del gestionale che permettere di inserire le informazioni del nuovo elemento.

![Creazione di un nuovo record (Anagrafiche)](../.gitbook/assets/Modal.gif)

### 📝 Modifica record

Cliccando su un singolo record è possibile accede alla schermata di dettaglio dello stesso, da cui è possibile andare ad apportarvi modifiche.

![](../.gitbook/assets/record.jpeg)

Per modificare le righe di un documento è possibile selezionare tutte le righe interessate e svolgere azioni di duplicazione o eliminazione massive.

![operazioni massive sulle righe documento](<../.gitbook/assets/immagine (66).png>)

### 🔧 Plugin

I plugin sono dei moduli che dipendono da altri moduli, e pertanto possono essere considerati dei sotto-moduli. Ogni modulo può possedere un numero variabile di plugin, che è possibile visualizzare nella sezione destra della pagina entrando in un record.

![](<../.gitbook/assets/immagine (24).png>)

{% hint style="info" %}
Per gli amministratori, è presente un plugin denominato **Info** che permette di visualizzare la cronologia del record
{% endhint %}

## 📍 Gestione dei moduli

Le operazioni di gestione dei moduli, quali abilitazione e disabilitazione, sono disponibili attraverso il modulo [Stato dei servizi](stato-dei-servizi.md). Da qui inoltre, abilitando il modulo _Viste,_ è possibile creare delle query personalizzate per cambiare la visualizzazione dei vari moduli.

## 💡 Campi personalizzati

{% hint style="warning" %}
Questa funzione è di rilevanza per chi desidera personalizzare alcune delle informazioni presentate dal gestionale senza modificare in modo consistente il codice generale.
{% endhint %}

A partire dalla versione 2.4 è possibile sfruttare dei campi personalizzati per aggiungere informazioni ai moduli principali in modo dinamico.

Questi campi sono gestiti a livello di database attraverso le tabelle `zz_fields` e `zz_field_record`, che si occupano rispettivamente della gestione generale dei campi e del salvataggio dei record personalizzati. Le procedure automatiche di gestione di questi campi sono integrate nei file `actions.php`, `editor.php` e `add.php`.

E' disponibile il modulo **Campi personalizzati**, da abilitare in Viste, per la gestione dinamica di queste informazioni.

#### _**Esempio di utilizzo**_

Volendo inserire un campo "Marca" selezionabile dalla videata articoli, la sintassi da utilizzare sarà la seguente:

```
// {[ "type": "select", "label": "Marca", "name": "|name|", "values": "list=\"\": \"Nessuno\", \"ValoreUno\": \"EtichettaUno\", \"ValoreDue\": \"EtichettaDue\", \"altro\": \"Altro\"", "value":"|value|"]}
```

{% hint style="warning" %}
E' importante utilizzare i valori |name| e |value| come suggerito dalle istruzioni per il campo contenuto presenti nella parte inferiore della pagina, affinchè i record vengano salvati correttamente.
{% endhint %}

![](<../.gitbook/assets/immagine (4).png>)

Questo produrrà la creazione di un campo "Marca" all'interno dei record del modulo Articoli:

![](<../.gitbook/assets/immagine (13).png>)

{% hint style="danger" %}
I campi creati in questo modo sono difficili da gestire nelle query del gestionale.
{% endhint %}
