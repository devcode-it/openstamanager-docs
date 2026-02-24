---
description: Come utilizzare i framework per personalizzare OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/I8PynmXUVfCOtwZFC1I6/per-sviluppatori/base/framework
---

# 🖥️ Framework

> Un framework, termine della lingua inglese che può essere tradotto come intelaiatura o struttura, in informatica e specificatamente nello sviluppo software, è un'architettura logica di supporto (spesso un'implementazione logica di un particolare design pattern) su cui un software può essere progettato e realizzato, spesso facilitandone lo sviluppo da parte del programmatore.
>
> [Wikipedia](https://it.wikipedia.org/wiki/Framework)

Il progetto utilizza [Composer](https://getcomposer.org/) per gestire le librerie PHP in modo completamente gratuito e opensource. Questo permette di completare l'installazione e l'aggiornamento dei diversi framework in modo facile ed intuitivo, senza doversi preoccupare in modo eccessivo delle dipendenze delle diverse librerie.

## Struttura

I framework vengono automaticamente scaricati da Composer all'interno della cartella _vendor_ nella root del progetto, dove vengono memorizzati secondo un percorso derivante dall'origine del pacchetto (per maggiori informazioni, consultare la [documentazione ufficiale di Composer](https://getcomposer.org/doc/)).

La modifica dei contenuti di `vendor` è altamente sconsigliata, poichè qualunque aggiornamento potrebbe sovrascrivere ed annullare le modifiche effettuate.

## Personalizzazione

{% hint style="info" %}
Nel caso si rivelasse necessario aggiornare i framework presenti o installare nuove librerie, è necessario avere disponibile una corretta e funzionante [installazione locale di Composer](https://getcomposer.org/download/).

Una volta completata l'installazione di Composer è possibile, partendo dalla cartella del gestionale, iniziare l'aggiornamento e la personalizzazione tramite le seguenti operazioni.
{% endhint %}

### Aggiornamento

L'aggiornamento dei framework è effettuabile tramite il seguente comando:

```bash
php composer.phar update
```

Per ulteriori informazioni, consultare la [documentazione ufficiale di Composer](https://getcomposer.org/doc/).

### Installazione di nuovi pacchetti

Per installare nuovi framework e/o librerie è utilizzabile il seguente comando:

```bash
php composer.phar require <package>
```

Per ulteriori informazioni, consultare la [documentazione ufficiale di Composer](https://getcomposer.org/doc/).

## Framework predefiniti

* davidepastore/codice-fiscale
* devcode-it/ical-easy-reader
* devcode-it/sdd\_ita
* digitick/sepa-xml
* doctrine/sql-formatter
* dragonmantank/cron-expression
* endroid/qr-code
* ezyang/htmlpurifier
* filp/whoops
* greenlion/php-sql-parser
* guzzlehttp/guzzle
* ifsnop/mysqldump-php
* illuminate/database
* intervention/image
* jurosh/pdf-merge
* league/csv
* league/flysystem
* league/flysystem-ftp
* league/oauth2-client
* league/oauth2-google
* monolog/monolog
* mpdf/mpdf
* owasp/csrf-protector-php
* phpmailer/phpmailer
* picqer/php-barcode-generator
* respect/validation
* servo/fluidxml
* slim/flash
* spipu/html2pdf
* symfony/filesystem
* symfony/finder
* symfony/polyfill-ctype
* symfony/translation
* symfony/var-dumper
* thenetworg/oauth2-azure
* voku/stringy
* willdurand/geocoder

_I nomi sono indicati secondo la notazione tipica dei progetti pubblici su GitHub._
