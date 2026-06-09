---
description: Guida al modulo aggiuntivo E-commerce in OpenSTAManager
---

# 📗 E-commerce

{% hint style="info" %}
Il modulo è dedicato alla **gestione delle operazioni di sincronizzazione** del gestionale con servizi esterni attraverso una procedura basata sul concetto di importazione ed esportazione dei dati.
{% endhint %}

{% hint style="warning" %}
La **sincronizzazione** è attualmente gestita con le piattaforme di e-commerce PrestaShop, WooCommerce e Shopify, in questo modo:
{% endhint %}

### Piattaforme supportate

#### Importazione da ecommerce

| Provider    | Versione | Articoli | Marche | Q.tà | Ordini | Anagrafiche |
| ----------- | -------- | -------- | ------ | ---- | ------ | ----------- |
| Prestashop  | >= 1.7.0 | ✅        | ✅      | ✅    | ✅      | ✅           |
| Woocommerce | >= 7.0   | ✅        | ⬜      | ⬜    | ✅      | ⬜           |
| Shopify     | >= 2.0   | ✅        | ⬜      | ✅    | ✅      | ✅           |

#### Esportazione da OSM

| Provider    | Versione | Articoli | Marche | Q.tà | Ordini | Anagrafiche |
| ----------- | -------- | -------- | ------ | ---- | ------ | ----------- |
| Prestashop  | >= 1.7.0 | ✅        | ✅      | ✅    | ⬜      | ⬜           |
| Woocommerce | >= 7.0   | ✅        | ⬜      | ✅    | ✅      | ✅           |
| Shopify     | >= 2.0   | ⬜        | ⬜      | ✅    | ⬜      | ⬜           |

{% hint style="warning" %}
La sincronizzazione delle marche, combinazioni articolo e delle funzionalità non selezionate nella tabella sono ancora in via di sviluppo.
{% endhint %}

{% hint style="info" %}
Il modulo è stato testato con la sincronizzazione di circa 1000 records per ciascuna risorsa (anagrafiche, articoli e ordini).
{% endhint %}

{% hint style="success" %}
[Clicca qui](https://shop.openstamanager.com/prodotto/e-commerce/) per procedere all'acquisto
{% endhint %}

### Installazione e Configurazione

A seguito dell'installazione del modulo, cliccando su **Sincronizzazione** apparirà alla destra la seguente schermata di configurazione.

<figure><img src="../.gitbook/assets/immagine (1465).png" alt=""><figcaption></figcaption></figure>

#### Impostazioni principali

* **URL del servizio**: è l'indirizzo del sito web di E-commerce
* **Token di accesso**: è la chiave generata dal provider per poter interagire con i web services
  * **PrestaShop**: https://www.edupass.it/manuali/manualistica-passweb/manuale-siti-ecommerce?a=manuale-passweb-ecommerce/marketplace/altri-marketplace/prestashop/attivazione-api-prestashop
  * **WooCommerce**: https://woocommerce.com/document/woocommerce-rest-api/#section-2
* **Debug abilitato**: se attivato mostra l'eventuale avviso di errore in fase di esportazione/importazione.
* **Categorie da sincronizzare**: menù a tendina multiplo che permette di esportare sul sito di E-commerce solo gli articoli delle categorie selezionate.
* **Disabilita articoli con quantità nulla**: se questa impostazione è attiva, in fase di esportazione articoli viene disattivata la visualizzazione sul sito di E-commerce se la quantità è a 0 e quindi non disponibile a magazzino.
* **Sincronizza solo articoli con foto impostata**: questa impostazione esporta solo gli articoli che hanno una foto impostata nella scheda articolo di OSM
* **Gestione locale delle immagini articolo**: se attivata, in fase di importazione articoli aggiorna l'immagine dell'articolo su OSM
* **Importazione in OpenSTAManager**: permette l'importazione degli articoli dal provider a OpenSTAmanager
* **Esportazione da OpenSTAManager**: permette l'esportazione degli articoli da OpenSTAManager al provider

<figure><img src="../.gitbook/assets/immagine (1466).png" alt=""><figcaption></figcaption></figure>

Ogni modifica effettuata nella sezione Impostazioni viene aggiornata premendo il pulsante **Salva** presente in alto a destra nella schermata.

> **Attenzione:** Prima di procedere con la prima sincronizzazione consigliamo di eseguire un Backup.

### Procedura di Sincronizzazione

Una volta configurate le impostazioni del modulo E-commerce è possibile eseguire manualmente la sincronizzazione selezionando una risorsa da importare/esportare e premendo successivamente **Avvia**.

La procedura di sincronizzazione avviene in due fasi:

1. Richiesta AJAX per ottenere l'elenco dei record da sincronizzare
2. Suddivisione dei record in gruppi ristretti (20 elementi), per cui viene effettuata una richiesta AJAX per l'effettiva sincronizzazione in modo sequenziale e separato

### Troubleshooting

Se l'esportazione va in errore, provare a collegarsi alle api del webservice, digitando dal browser l'url dell'E-commerce, aggiungendo "/api" all'url e inserendo come password il token corrispondente.

Se non vengono visualizzate le risorse disponibili sarà necessario inserire nel file `.htaccess` del webservice la seguente stringa:

```apache
RewriteEngine on
RewriteCond %{HTTP:Authorization} ^(.*)
RewriteRule . - [E=HTTP_AUTHORIZATION:%1]
```

### Plugin Info sincronizzazione

Per definire i campi da esportare è accessibile un nuovo plugin **Info sincronizzazione** che è presente nel menù di destra nella schermata di modifica degli Articoli. In questa sezione è possibile definire le informazioni aggiuntive che verranno sincronizzate nell'E-commerce con la possibilità di disattivare l'articolo dalla sincronizzazione.

### Utilizzo API e Task

Sono disponibili alcune risorse API per automatizzare le procedure di sincronizzazione. Le risorse API in questione sono di tipo `create` (POST per l'esportazione) e `update` (PUT per l'importazione), e necessitano il parametro `connection_name` per individuare la connessione da utilizzare.

#### Elenco API disponibili:

* `sincro-articoli`

In modo simile, sono disponibili delle task di cron (da registrare manualmente) distinte per l'importazione e l'esportazione. Queste task considerano sempre la prima connessione configurata per il modulo.

#### Elenco task disponibili:

* `EsportazioneArticoli`
* `ImportazioneArticoli`

### Webhooks Shopify

Per Shopify sono disponibili dei webhook specifici per la sincronizzazione automatica:

* `shopify_webhooks/shopify_articoli.php`: sincronizzazione articoli
* `shopify_webhooks/shopify_giacenze.php`: sincronizzazione giacenze
* `shopify_webhooks/shopify_ordini.php`: sincronizzazione ordini

Questi webhook permettono di aggiornare automaticamente i dati in OpenSTAManager quando avvengono modifiche su Shopify.

***

### Changelog

#### 5.0 (2026-03-10)

**Aggiunto (Added)**

* Aggiunta file JSON per controlli integrità gestionale
* Aggiunta gulpfile e package.json per automazione build
* Aggiunta rector e php-cs-fixer per refactoring automatico e formattazione codice

**Modificato (Changed)**

* Formattazione stile codice per uniformità

#### 4.0 (2025-10-03)

**Aggiunto (Added)**

* Aggiunta importazione articoli e ordini da woocommerce
* Aggiunta esportazione ordini, categorie e anagrafiche su woocommerce

**Corretto (Fixed)**

* Corretta esportazione articoli su woocommerce

#### 3.0 (2024-12-09)

**Modificato (Changed)**

* Rimosso modulo Marchi, presente in release

#### 2.0 (2024-11-13)

**Modificato (Changed)**

* Ottimizzato codice per php8.3 e OSM 2.5

#### 1.6 (2024-01-16)

**Aggiunto (Added)**

* Aggiunta sincronizzazione con Shopify
* Aggiunta php-cs-fixer

#### 1.5 (2023-09-04)

**Aggiunto (Added)**

* Aggiunta hugo-documentazione
