---
description: Guida alle azioni aggiuntive del modulo Ordini cliente di OpenSTAManager
icon: circle-question
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/WzoKFijlVGKTMgti0acZ/openstamanager/modules/vendite/ordinicliente/plugin1
---

# Azioni aggiuntive

## Dal modulo Ordini cliente

Il modulo ordini cliente permette di fatturare massivamente e cambiare massivamente lo stato degli ordini cliente dalle azioni di gruppo.

### Fattura contratti

Una volta selezionati i record interessati è possibile fatturare massivamente i contratti cliccando su Azioni di gruppo/Fattura ordini cliente.

{% hint style="info" %}
Lo stato dell'ordine cliente deve essere Accettato.
{% endhint %}

![](<../../../../.gitbook/assets/immagine (737).png>)

Il gestionale chiederà quindi la conferma a procedere alla fatturazione, permettendo di scegliere:

* Se aggiungere le righe degli ordini cliente selezionati a una fattura di vendita in bozze dello stesso cliente
* il sezionale in cui andare a registrare la fattura di vendita
* il tipo di documento che si andrà a creare

Cliccando su procedi si confermerà la fatturazione.

&#x20;                                                 <img src="../../../../.gitbook/assets/immagine (447).png" alt="" data-size="original">

Sarà ora possibile visualizzare la fattura di vendita appena creata nel modulo Vendite/Fatture di vendita.

![](<../../../../.gitbook/assets/immagine (696).png>)

![](<../../../../.gitbook/assets/immagine (603).png>)

### Modifica dello stato massivo

Una volta selezionati i record interessati è possibile modificarne lo stato massivamente cliccando su Azioni di gruppo/Cambia stato.

![](<../../../../.gitbook/assets/immagine (681).png>)

Il gestionale chiederà quindi la conferma a procedere alla modifica dello stato, permettendo di scegliere tra gli stati presenti:

* Bozza
* Evaso
* Parzialmente evaso
* Parzialmente fatturato
* Fatturato
* In attesa di conferma
* Accettato
* Annullato

&#x20;                                                  <img src="../../../../.gitbook/assets/immagine (867).png" alt="" data-size="original">

Cliccando su Procedi si confermerà l'operazione.

## Dal dettaglio Ordine cliente

Cliccando su uno specifico record è possibile entrare nella schermata di dettaglio.

Da qui, nella sezione superiore della pagina, è possibile trovare le funzioni:

* Stampa ordine cliente
* Invia ordine
* Crea...

### Stampa ordine cliente

Dalla schermata di dettaglio di un ordine cliente è possibile procedere a diversi tipi di stampe:

* ordine cliente
* consuntivo ordine
* ordine cliente (senza codici)
* ordine cliente (senza prezzi)

![](<../../../../.gitbook/assets/immagine (698).png>)

Cliccando sul tipo di stampa scelto sarà possibile visualizzare la stampa del documento

&#x20;                                           ![](<../../../../.gitbook/assets/immagine (601).png>)

### Invia

Dalla schermata di dettaglio di un ordine cliente è possibile procedere a inviarlo via mail al cliente.

![](<../../../../.gitbook/assets/immagine (680).png>)

Cliccando su Invia ordine si verrà indirizzati al template email compilato con i dati dell'ordine cliente, dove sarà possibile inviare la mail cliccando su invia.

![](<../../../../.gitbook/assets/immagine (842).png>)

### Crea...

Dalla schermata di dettaglio di un ordine cliente è possibile procedere alla creazione di documenti collegati ad esso:

* Attività
* Ordine fornitore
* DDT
* Fattura

{% hint style="warning" %}
Nel preventivo deve essere presente almeno una riga, e lo stato del preventivo deve essere impostato su: Accettato, Rifiutato, In lavorazione, Concluso, Pagato, Fatturato o Parzialmente fatturato.
{% endhint %}

![](<../../../../.gitbook/assets/immagine (847).png>)

Cliccando sul tipo di azione da svolgere si verrà indirizzati alla schermata di creazione del tipo di documento selezionato, dove andare a definirne le specifiche.

![](<../../../../.gitbook/assets/immagine (835).png>)
