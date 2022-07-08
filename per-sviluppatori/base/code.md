---
title: Codice
sidebar:
  nav: docs-sidebar
description: Come modificare il codice di OpenSTAManager
---

# 🕹 Codice

OpenSTAManager presenta una struttura nativamente predisposta alla personalizzazione delle funzioni principali: di seguito verranno fornite le specifiche tecniche per modificare il codice dove previsto.

{% hint style="warning" %}
Ogni modifica sui file del gestionale potrebbe provocare errori e problematiche imprevedibili all'interno di OpenSTAManager. Si sconsiglia pertanto di non intraprendere queste azioni se non si è estremamente sicuri delle proprie conoscenza informatiche.
{% endhint %}

## 🏗️ Struttura

{% hint style="warning" %}
Per personalizzare un file è inizialmente necessario copiarlo all'interno della relativa cartella `custom/`.
{% endhint %}

Tutte le personalizzazioni del codice devono sempre essere inserite all'interno di una relativa cartella `custom/` della sezione che si vuole personalizzare:

* Modulo **Anagrafiche**: `modules/anagrafiche/custom`
* Plugin **Sedi**: `plugins/sedi/custom`
* Stampa **Intervento**: `templates/interventi/custom/`

### Cartella `include/`

OpenSTAManager supporta inoltre la personalizzazione di alcuni contenuti della cartella `include/`:

* File di gestione del layout
  * `top.php` per l'header
  * `bottom.php` per il footer
* Cartella `common/` con il layout di base per la maggior parte di righe/articoli dei moduli
* Cartella `extra/` per i contenuti personalizzati in alto ad ogni pagina
  * `login.php` per i contenuti al login
  * `extra.php` per i contenuti dopo il login

## 📓 Esempi

### 📓 Modifica ordine dei campi

Modulo considerato: **Anagrafiche**.

In base ai campi che si desidera riordinare, potrebbe essere necessario modificare sia il file `modules/anagrafiche/custom/edit.php` (schermata di modifica del record) che il file `modules/anagrafiche/custom/add.php` (schermata di creazione del record).

Se si desidera modificare l'ordine dei campi di un modulo nella modifica del record, per esempio _Luogo di nascita_ e _Data di nascita_, modificare il codice HTML di default

```markup
<div class="col-md-4">
    {[ "type": "text", "label": "<?php echo tr('Luogo di nascita'); ?>", "name": "luogo_nascita", "value": "$luogo_nascita$" ]}
</div>

<div class="col-md-4">
    {[ "type": "date", "label": "<?php echo tr('Data di nascita'); ?>", "maxlength": 10, "name": "data_nascita", "value": "$data_nascita$" ]}
</div>
```

nel seguente

```markup
<div class="col-md-4">
    {[ "type": "date", "label": "<?php echo tr('Data di nascita'); ?>", "maxlength": 10, "name": "data_nascita", "value": "$data_nascita$" ]}
</div>

<div class="col-md-4">
    {[ "type": "text", "label": "<?php echo tr('Luogo di nascita'); ?>", "name": "luogo_nascita", "value": "$luogo_nascita$" ]}
</div>
```

### 📓 Azioni aggiuntive

Modulo considerato: **Anagrafiche**.

Per cambiare l'azione che viene effettuta a seguito del _submit_ di un _form_ del modulo, è necessario modificare di conseguenza il file `modules/anagrafiche/custom/actions.php` dopo aver individuato il valore del campo **op** del _form_ in questione.

Valori standard del campo **op**:

* Creazione del record: `add`
* Modifica del record: `update`
* Eliminazione del record: `delete`

### 📓 Modifica del comportamento

Modulo considerato: **Fatture**.

In alcuni casi complessi, può essere necessario modificare più sezioni di codice all'interno del modulo e in sezioni separate. Un esempio può essere individuato nella gestione delle righe delle fatture di OpenSTAManager, nel caso si voglia inserire nel campo _Costo unitario_ il costo aggiuntivo di IVA.

In questo caso, le modifiche dovranno considerare numerosi file poichè il comportamento dovrà essere replicato in modo indipendete in tutte le procedure di creazione/modifica righe (file `modules/fatture/custom/actions.php` e `modules/fatture/custom/modutil.php`).

Una volta completata la gestione del modulo attraverso oggetti Eloquent, sarà possibile limitare la modifica ai soli file `modules/fatture/custom/src/Articolo.php` e `modules/fatture/custom/src/Riga.php` sovrascrivendo i metodi di base _setSubtotale_ e _setIdIvaAttribute_:

```php
public function fixSubtotale()
{
    $iva = database()->fetchOne('SELECT * FROM co_iva WHERE id = :id_iva', [
        ':id_iva' => $this->idiva,
    ]);

    $netto = $this->costo_unitario / (1 + $iva['percentuale'] / 100);
    $iva = $this->costo_unitario - $netto;

    $this->subtotale = $netto * $this->qta;
    $this->iva = $iva * $this->qta;

    $this->fixIvaIndetraibile();
}

public function fixIva()
{
    $iva = database()->fetchOne('SELECT * FROM co_iva WHERE id = :id_iva', [
        ':id_iva' => $this->idiva,
    ]);
    $descrizione = $iva['descrizione'];

    $this->desc_iva = $descrizione;

    $this->fixSubtotale();
    //$valore = ($this->subtotale - $this->sconto) * $iva['percentuale'] / 100;
    //$this->iva = $valore;
    //$this->iva_indetraibile = $valore / 100 * $iva['indetraibile'];
}
```

Ovviamente, bisognerà adeguare di conseguenza il file `modules/fatture/custom/row-edit.php` nella riga di individuazione del prezzo:

```php
$result['prezzo'] = ($riga['subtotale'] + $riga['iva']) / $riga['qta'];
```
