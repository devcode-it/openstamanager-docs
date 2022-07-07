---
title: Template email
description: Come creare un template email  OpenSTAManager
---

# 📃 Template email

{% hint style="info" %}
Il modulo **Template email** permette all’azienda di gestire le informazioni di base riguardanti i contenuti e le caratteristiche delle email che OpenSTAManager può eventualmente procedere a inviare.
{% endhint %}

Questo modulo è complementare a [**Account email**](account.md), che si occupa di gestire le informazioni degli account email utilizzati per l'invio delle email.

La schermata del modulo si presenterà così:

![](<../../.gitbook/assets/image (62) (1) (1) (1) (1).png>)

## ➕ Creazione

Per creare un nuovo template email si dovrà cliccare sul tasto (+) e inserire il Nome, Modulo a cui applicarlo, Oggetto e indirizzo email da cui inviare la mail.

![](<../../.gitbook/assets/image (29) (1) (1) (1) (1) (1).png>)

## 🖌️ Modifica

La schermata di modifica permette il completamento di tutte le informazioni riguardanti il template, vengono resi disponibili i seguenti attributi:

* Notifica di lettura (per richiederla)
* Icona
* CC
* CCN
* Rispondi a
* Stampe da allegare (di default)
* Mansioni
* Contenuto

![](<../../.gitbook/assets/image (76) (1) (1).png>)

Tra questi campi, _Contenuto_ e _Oggetto_ prevedono un sistema di autocompletamento per alcuni particolari valori definiti dal modulo. L'elenco completo di questi elementi viene reso disponibile nella sezione informativa **Variabili**.

![](<../../.gitbook/assets/image (68) (1) (1) (1) (1).png>)

La sostituzione di queste componenti dipende dai contenuti del _record_ da cui viene inviata l'email.

È inoltre presente il pulsante **Duplica template** che permette di duplicare un template precedentemente creato.

![](<../../.gitbook/assets/image (36) (1) (1) (1) (1) (1) (2).png>)

## 🪀 Particolarità

Sono presenti dei template predefiniti per diversi moduli, personalizzabili a piacimento.

{% hint style="info" %}
Inserendo un'indirizzo email nel campo "**CC**" di un relativo **Template** ogni email verrà inviata anche all'indirizzo email inserito in "**CC"** oltre al destinatario principale dell'email. Questo, per esempio, può essere utile se voglio inviare un'email ad un **Cliente** e al commercialista.
{% endhint %}
