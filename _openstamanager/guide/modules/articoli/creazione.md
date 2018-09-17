---
title: Creazione articolo
---

La creazione di nuovi elementi segue il funzionamento standard del gestionale, necessitando il click sul pulsante apposito all'interno dell'intestazione del modulo.

Il modulo **Articoli** presenta quindi la possibilità di inserire le informazioni complete relativa alla nuova attività da creare.

{% include figure path="add.png" alt="Creazione di un nuovo record" caption="Schermate di creazione di una nuova attività" %}

## Caratteristiche

Il sistema di creazione di un nuovo elemento richiede la compilazione di alcune informazioni fondamentali:
 - Codice dell'articolo
 - Nome completo dell'articolo
 - Categoria
 - Eventuale sottocategoria

### Creazione categoria al volo

Nella schermata di creazione di un nuovo articolo viene permessa la creazione al volo delle **Categorie** relative al nuovo *record*.
Questa funzionalità viene permessa dal pulsante dedicato a destra del selettore del campo *Categoria*.

{% include figure path="select.png" alt="Pulsante di creazione al volo" caption="Pulsante di creazione categoria al volo" %}

La gestione della creazione viene quindi delegata al modulo **Categorie**, permettendo l'inserimento delle informazioni standard previste attraverso un *modal* sovrapposto al resto del contenuto:
 - Nome
 - Colore
 - Nota

{% include figure path="fast-add.png" alt="Schermata di creazione anagrafica" caption="Schermata di creazione di una nuova anagrafica" %}

Una volta completata la creazione in questione, la categoria creata verrà automaticamente selezionata.
{% include figure path="auto-select.png" alt="Selezione automatica" caption="Effetto di selezione automatica della nuova anagrafica" %}

Lo stesso procedimento è disponibile per il campo *Sottocategoria*.
{: .notice-warning }

