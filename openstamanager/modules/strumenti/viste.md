---
description: Come gestire le Viste in OpenSTAManager
icon: eye
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/UK4SVx7wuArwVldJWR1I/openstamanager/modules/strumenti/viste
---

# Viste

{% hint style="info" %}
Il modulo **Viste** permette di apportare delle modifiche alle tabelle contenenti i dati di ciascun modulo.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

## Modifica

Cliccando sul record da modificare si aprirà la schermata di dettaglio, in cui si potranno notare diverse sezioni:

* Opzioni generali
* Campi disponibili
* Ordine di visualizzazione

### Opzioni generali

Grazie a **Opzioni generali** è possibile modificare diversi campi, quali:

* Nome del modulo (modificare il nome che identifica il modulo)
* Query personalizzata (scrivere una query in sostituzione a quella di default)

<figure><img src="../../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

Nelle query è possibile utilizzare dei segnaposto che verranno sostituiti come fossero delle variabili:

* **|select|**: viene sostituito con la lista dei campi da visualizzare definiti sotto
* **|date\_period(co\_documenti.data)|**: viene sostituito con "AND WHERE co\_documenti.data BETWEEN "data\_inizio" AND "data\_fine". "data\_inizio" e "data\_fine" vengono valorizzati in base al filtro di date selezionabile dal menu in alto a sinistra\
  \_\_![](<../../../.gitbook/assets/image (373).png>)\\
* **1=1**: è necessario specificarlo subito dopo il WHERE per far sì che venga sostituito automaticamente con i filtri che l'utente digita nel modulo. In questo modo il sistema sa dove innestare i vari filtri tramite WHERE
* **2=2**: è come 1=1 ma funzione sulla clausola HAVING, utile per le ricerche tramite HAVING

### Campi disponibili

Nella sezione **Campi disponibili** è possibile cambiare:

* Gruppi con accesso (gruppi e utenti in grado di visualizzare quel campo)
* Visibilità (stato del campo, visualizzabile oppure nascosto)

<figure><img src="../../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

Cliccando sopra un _record_ è possibile definire diverse opzioni:

* Ricercabile (indica se il campo è ricercabile)
* Ricerca lenta (selezionabile per indicare se la ricerca di quel campo è lenta)
* Ricerca tramite
* Calcolo a fine colonna (è possibile impostare la somma o la media)
* Formattazione automatica
* Abilitare o disabilitare l'utilizzo dell'HTML nel campo
* Ordina tramite

<figure><img src="../../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

Per aggiungere delle colonne alle viste, quindi dei campi non presenti tra quelli elencati, si deve copiare la query presente nel campo **Query di default** nel campo **Query personalizzata**, andando ad apportare le dovute modifiche.

{% hint style="danger" %}
Nel caso in cui la query non sia scritta correttamente, la vista non riporterà piu alcun risultato.
{% endhint %}

### Ordine di visualizzazione

Nella sezione **Ordine di visualizzazione** si può cambiare l'ordine dei campi trascinandoli:

<figure><img src="../../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

### Esempi di personalizzazione viste

{% content-ref url="../../../guide/esempi/formattazione-celle.md" %}
[formattazione-celle.md](../../../guide/esempi/formattazione-celle.md)
{% endcontent-ref %}
