---
description: Come creare un template email  OpenSTAManager
icon: circle
---

# Template email

{% hint style="info" %}
Il modulo **Template email** permette all’azienda di gestire le informazioni di base riguardanti i contenuti e le caratteristiche delle email che OpenSTAManager può eventualmente procedere a inviare.
{% endhint %}

Questo modulo è complementare a [**Account email**](account.md), che si occupa di gestire le informazioni degli account email utilizzati per l'invio delle email.

La schermata del modulo si presenterà così:

<figure><img src="../../../.gitbook/assets/immagine (216).png" alt=""><figcaption></figcaption></figure>

## Creazione

Per creare un nuovo template email si dovrà cliccare sul tasto (+) e inserire il Nome, Modulo a cui applicarlo, Oggetto e indirizzo email da cui inviare la mail.

<figure><img src="../../../.gitbook/assets/immagine (217).png" alt=""><figcaption></figcaption></figure>

## Modifica

La schermata di modifica permette il completamento di tutte le informazioni riguardanti il template, vengono resi disponibili i seguenti attributi:

* Notifica di lettura (per richiederla)
* Icona
* CC
* CCN
* Rispondi a
* Stampe da allegare (di default)
* Mansioni
* Contenuto

<figure><img src="../../../.gitbook/assets/immagine (1324).png" alt=""><figcaption></figcaption></figure>

Tra questi campi, _Contenuto_ e _Oggetto_ prevedono un sistema di autocompletamento per alcuni particolari valori definiti dal modulo. L'elenco completo di questi elementi viene reso disponibile nella sezione informativa **Variabili**.

<figure><img src="../../../.gitbook/assets/immagine (219).png" alt=""><figcaption></figcaption></figure>

La sostituzione di queste componenti dipende dai contenuti del _record_ da cui viene inviata l'email.

È inoltre presente il pulsante **Duplica template** che permette di duplicare un template precedentemente creato.

<figure><img src="../../../.gitbook/assets/immagine (220).png" alt=""><figcaption></figcaption></figure>

## Particolarità

Sono presenti dei template predefiniti per diversi moduli, personalizzabili a piacimento.

{% hint style="info" %}
Inserendo un'indirizzo email nel campo "**CC**" di un relativo **Template** ogni email verrà inviata anche all'indirizzo email inserito in "**CC"** oltre al destinatario principale dell'email. Questo, per esempio, può essere utile se voglio inviare un'email ad un **Cliente** e al commercialista.
{% endhint %}
