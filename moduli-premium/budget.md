---
description: Guida al modulo premium Budget in OpenSTAManager
metaLinks:
  alternates:
    - https://app.gitbook.com/s/I8PynmXUVfCOtwZFC1I6/moduli-premium/budget
---

# 📗 Budget

**Budget** è uno dei diversi moduli acquistabili da **OpenSTAManager.** Permette di visualizzare sotto forma di grafico e tabella l'**andamento economico** (costi/ricavi) e l'**andamento finanziario** (entrate/uscite). Oltre all'andamento reale, permette di integrare anche le **previsioni di costi e ricavi**, e delle **entrate** e **uscite**.

{% hint style="info" %}
[Clicca qui](https://shop.openstamanager.com/prodotto/budget/) per procedere all'acquisto.
{% endhint %}

A seguito dell'installazione del modulo, cliccando su **Budget** apparirà il seguente prospetto che evidenzia l'**Utile totale**, dato dalla differenza tra ricavi e costi totali.

<figure><img src="../.gitbook/assets/immagine (1435).png" alt=""><figcaption></figcaption></figure>

#### Componenti principali

* **Grafico**: Visualizzazione grafica dell'andamento economico e finanziario
* **Tabella**: Dati dettagliati per periodo
* **Utile totale**: Differenza tra ricavi e costi

### 💰 Andamento economico

L'andamento economico analizza i **costi** e i **ricavi** dell'azienda.

#### Ricavi

I ricavi sono composti da due elementi:

1. **Ricavi reali**: Somma delle fatture di vendita già contabilizzate
2. **Ricavi totali**: Somma dei ricavi reali + ricavi previsti da previsionali o sorgenti esterne

#### Costi

I costi seguono la stessa logica dei ricavi:

* **Costi reali**: Somma delle fatture di acquisto già contabilizzate
* **Costi totali**: Somma dei costi reali + costi previsti da previsionali o sorgenti esterne

<figure><img src="../.gitbook/assets/immagine (1436).png" alt=""><figcaption></figcaption></figure>

***

### 💵 Andamento finanziario

L'andamento finanziario analizza le **entrate** e le **uscite** effettive o previste.

#### Caratteristiche principali

A differenza dell'andamento economico, l'andamento finanziario:

* **Attinge dati anche dallo scadenzario**
* **Imputa tutte le scadenze previste** nel relativo periodo di competenza
* Considera l'importo **lordo** (IVA inclusa)

#### Distribuzione dei pagamenti

La previsione di entrata/uscita considera l'importo lordo e lo distribuisce in base al:

* **Tipo di pagamento specificato nel documento**
* **Pagamento legato all'anagrafica** (se mancante nel documento)

***

### 🔮 Previsionale

Le previsioni economiche sono configurabili dal sotto-menu **"Previsionale"**.

<figure><img src="../.gitbook/assets/immagine (1437).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/immagine (1438).png" alt=""><figcaption></figcaption></figure>

#### Funzionalità

Dal menu Previsionale è possibile:

* **Creare previsioni di costi e ricavi**
* **Selezionare la ricorrenza** delle previsioni
* **Gestire periodi temporali** specifici

#### Ricorrenze supportate

Le previsioni possono essere configurate con diverse ricorrenze:

* Mensile
* Trimestrale
* Semestrale
* Annuale
* Personalizzata

***

### 🔌 Sorgenti esterne

Le sorgenti esterne permettono di integrare nel previsionale dati provenienti da altre aree di OpenSTAManager.

#### Sorgenti predefinite

Tra le sorgenti esterne sono inserite di default delle query che è possibile abilitare o disabilitare:

1. **DDT**: Ricavi provenienti da DDT accettati ma non ancora evasi
2. **Ordini clienti**: Ricavi da ordini clienti accettati ma non ancora evasi

#### Query SQL personalizzate

Per utenti avanzati (o su richiesta ai tecnici OpenSTAManager) è possibile configurare delle query SQL personalizzate per inserire ulteriori previsioni.

**Esempio: Previsione di ricavo da preventivo**

```sql
SELECT 
    (totale) AS totale,
    (descrizione) AS descrizione,
    (data) AS data,
    (scaduto) AS scaduto,
    (anagrafica) AS anagrafica
FROM ...
```

#### Requisiti delle query

Le query devono restituire almeno questi 4 campi:

* **totale**: Rappresenta l'importo da calcolare nel previsionale
* **descrizione**: Descrizione visualizzata nel previsionale
* **data**: Data in cui far ricadere la previsione
* **scaduto**: 1 per marcare la scadenza come scaduta (raggruppata nella popup di dettaglio)
* **anagrafica**: Nome dell'anagrafica a cui imputare la previsione

#### Query di esempio

**Previsionale entrate da contratti**

```sql
SELECT 
    ( ( (`co_righe_contratti`.`subtotale`-`co_righe_contratti`.`sconto`)/`co_righe_contratti`.`qta`)*(`co_righe_contratti`.`qta`-`co_righe_contratti`.`qta_evasa`) ) AS totale,
    CONCAT('Contratto ', `co_contratti`.`numero`, ': ', `co_righe_contratti`.`descrizione`) AS descrizione, 
    IF( `co_righe_contratti`.`data_fatturazione` < CURDATE(), CURDATE(), `co_righe_contratti`.`data_fatturazione`) AS data,
    IF( `co_righe_contratti`.`data_fatturazione` < CURDATE(), 1, 0) AS scaduto,
    an_anagrafiche.ragione_sociale AS anagrafica
FROM 
    `co_righe_contratti` 
    INNER JOIN `co_contratti` ON `co_contratti`.`id`=`co_righe_contratti`.`idcontratto` 
    INNER JOIN `an_anagrafiche` ON an_anagrafiche.idanagrafica=co_contratti.idanagrafica
WHERE 
    LAST_DAY( IF( `co_righe_contratti`.`data_fatturazione` < CURDATE(), CURDATE(), `co_righe_contratti`.`data_fatturazione`) ) = LAST_DAY('|anno|-|mese|-01')
    AND NOT `co_righe_contratti`.`is_descrizione`=1
    AND NOT (`co_righe_contratti`.`qta`-`co_righe_contratti`.`qta_evasa`) = 0
```

**Previsionale incassi da contratti**

```sql
SELECT 
    (( (`co_righe_contratti`.`subtotale`-`co_righe_contratti`.`sconto`)/`co_righe_contratti`.`qta`)*(`co_righe_contratti`.`qta`-`co_righe_contratti`.`qta_evasa`)*IFNULL(pagamenti2.prc/100, 1)+( (`co_righe_contratti`.`subtotale`-`co_righe_contratti`.`sconto`)/`co_righe_contratti`.`qta`)*(`co_righe_contratti`.`qta`-`co_righe_contratti`.`qta_evasa`)*IFNULL(pagamenti2.prc/100, 1)/100*IFNULL(co_iva.percentuale, '|iva_predefinita|' )) AS totale,
    CONCAT('Contratto ', `co_contratti`.`numero`, ': ', `co_righe_contratti`.`descrizione`) AS descrizione, 
    IF( `co_righe_contratti`.`data_fatturazione` + INTERVAL IFNULL(pagamenti2.num_giorni, 0) DAY < CURDATE(), CURDATE(), `co_righe_contratti`.`data_fatturazione` + INTERVAL IFNULL(pagamenti2.num_giorni, 0) DAY) AS data,
    IF( `co_righe_contratti`.`data_fatturazione` + INTERVAL IFNULL(pagamenti2.num_giorni, 0) DAY < CURDATE(), 1, 0) AS scaduto,
    an_anagrafiche.ragione_sociale AS anagrafica
FROM 
    `co_righe_contratti` 
    INNER JOIN `co_contratti` ON `co_contratti`.`id`=`co_righe_contratti`.`idcontratto` 
    INNER JOIN `an_anagrafiche` ON an_anagrafiche.idanagrafica=co_contratti.idanagrafica
    LEFT JOIN co_iva ON co_iva.id=an_anagrafiche.idiva_vendite
    LEFT JOIN co_pagamenti ON an_anagrafiche.idpagamento_vendite=co_pagamenti.id
    LEFT JOIN co_pagamenti AS pagamenti2 ON co_pagamenti.descrizione=pagamenti2.descrizione
WHERE 
    LAST_DAY( IF( `co_righe_contratti`.`data_fatturazione` + INTERVAL IFNULL(pagamenti2.num_giorni, 0) DAY < CURDATE(), CURDATE(), `co_righe_contratti`.`data_fatturazione` + INTERVAL IFNULL(pagamenti2.num_giorni, 0) DAY) ) = LAST_DAY('|anno|-|mese|-01')
    AND NOT `co_righe_contratti`.`is_descrizione`=1
    AND NOT (`co_righe_contratti`.`qta`-`co_righe_contratti`.`qta_evasa`) = 0
```

***

### 📄 Dettagli dei documenti

Per analizzare nel dettaglio tutti i documenti che concorrono a costituire il valore di entrate e uscite:

1. **Cliccare sull'importo interessato** nella tabella
2. Si aprirà una schermata con i riferimenti alle diverse fatture

Questa funzionalità permette di:

* Visualizzare l'elenco completo dei documenti
* Accedere direttamente ai documenti originali
* Verificare la composizione degli importi

***

### 📚 Conti per ricavi e costi

Cliccando sul tasto **"+"** vicino a Ricavi e Costi, sarà possibile vedere la lista dei conti in cui:

* **Ricavi** saranno imputati
* **Costi** saranno imputati

Questa visualizzazione permette di:

* Verificare la corretta contabilizzazione
* Identificare i conti di contabilità generale utilizzati
* Effettuare verifiche contabili

***

### ⚖️ Differenze tra andamento economico e finanziario

#### Andamento economico

* **Calcola costi e ricavi** al netto di IVA
* **Previsione per intero** in base alla data del documento
* **Data di competenza**: data del documento
* **Fonte dati**: fatture contabilizzate + previsionali

#### Andamento finanziario

* **Calcola entrate e uscite** al lordo di IVA
* **Distribuisce l'importo** in base al tipo di pagamento
* **Data di competenza**: date delle scadenze di pagamento
* **Fonte dati**: scadenzario + fatture + previsionali

***

### 📝 Esempi pratici

#### Esempio 1: Fattura con Ri.Ba. a 30/60gg

Avendo una fattura di **100€** (+ IVA ordinaria 22%) dovendola pagare con Ri.Ba. a 30/60gg:

**Andamento economico:**

* Ricavo: 100€ (imputato alla data della fattura)

**Andamento finanziario:**

* Totale lordo: 122€ (100€ + 22€ IVA)
* Primo pagamento: 61€ a 30 giorni
* Secondo pagamento: 61€ a 60 giorni

#### Esempio 2: Confronto con widget

Per confrontare il widget del fatturato o degli acquisti con i ricavi o i costi:

* **Sottrarre dal budget** tutti i movimenti di prima nota che non sono stati generati automaticamente all'emissione della fattura
* **Verificare la corrispondenza** delle date tra fattura e competenza
* **Controllare** che non ci siano movimenti con data diversa dalla data di competenza della fattura
