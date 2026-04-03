---
description: Come modificare lo stile delle tabelle in OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/guide/esempi/formattazione-celle
---

# 🌈 Formattazione celle

Con OpenSTAManager è possibile modificare la formattazione di una cella in base al valore previsto, da Strumenti/Viste.

Sarà sufficiente creare un nuovo campo utilizzando questi Nomi:

* **color\_Nome:** colore esadecimale della cella
* **color\_title\_Nome:** etichetta della cella colorata (es. campo relazione in anagrafica)
* **\_bg\_:** colore esadecimale della riga (es. campo Attività del colore dello stato attività)
* **\_print\_:** visualizza un'icona di una stampante che al click porta alla stampa utilizzando il valore di questo campo per definire quale template usare. Ad esempio nelle attività è valorizzata fissa a "intervento", questo significa che al click sul pulsante di stampa viene usato il template di stampa dentro templates/intervento/ e passa il campo id come id del record da stampare (es. attività)
* **icon\_Nome:** visualizza un'icona di FontAwesome ([https://fontawesome.com/v4/icons/](https://fontawesome.com/v4/icons/)) nella colonna di nome Nome
* **icon\_title\_Nome:** oltre all'icona aggiunge a fianco anche la descrizione dell'icona (es. lo stato di un ordine)

{% hint style="warning" %}
Si dovrà sostituire Nome con il nome del campo interessato.
{% endhint %}

#### Esempio

Nel modulo Magazzino/Articoli, si vuole evidenziare in rosso un record quando la quantità scende sotto le 5 unità.

Si dovrà andare in Strumenti/Viste/Articoli e creare un nuovo campo, con Query prevista:

```
IF(`qta`<5, 'red', '')
```

![](<../../.gitbook/assets/immagine (1034).png>)

{% hint style="warning" %}
Per poter abilitare il campo è importante che il campo Gruppi con accesso sia compilato con i tipi di utenti che dovranno visualizzarlo.
{% endhint %}

In questo modo l'effetto generato sarà il seguente:

![](<../../.gitbook/assets/immagine (440).png>)

Nel caso in cui invece si voglia modificare una determinata colonna in base al suo valore, si dovrà utilizzare color\_Nome. Volendo quindi creare una cella che diventi rossa in caso di quantità inferiore a 5 o verde in caso la quantità sia maggiore, si dovrà utilizzare:

```
IF(`qta`<5, 'red', '#008000')
```

![](<../../.gitbook/assets/immagine (536).png>)

Il risultato ottenuto sarà il seguente:

![](<../../.gitbook/assets/immagine (837).png>)

{% hint style="warning" %}
Si consiglia di utilizzare i colori in formato esadecimale.
{% endhint %}
