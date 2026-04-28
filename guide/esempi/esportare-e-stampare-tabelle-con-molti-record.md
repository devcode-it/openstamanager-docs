---
description: >-
  Come gestire le tabelle con molti record in fase di esportazione in Excel o
  stampa con OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/imnORsInuaaXiiRnlr6m/guide/esempi/esportare-e-stampare-tabelle-con-molti-record
---

# 👍 Esportare e stampare tabelle con molti record

{% hint style="info" %}
In OpenSTAManager è presente un filtro che limita il caricamento dei record delle tabelle per non subire rallentamenti nel caso di tabelle di grandi dimensioni.
{% endhint %}

Questo però, non permette di scaricare tutti i record in caso di esportazione.

Per poter esportare tutti i record di una tabella è necessario andare in Strumenti/Impostazioni/Generali/**Lunghezza in pagine del buffer Datatables.**

Si dovrà ora impostare il valore di questo campo a 100, permettendo il caricamento di tutte le pagine per poter eseguire una corretta esportazione.

Una volta terminata l'esportazione (che richiederà più tempo di un normale caricamento, in proporzione al numero di record presenti nel database) è consigliato ripristinare il valore della **Lunghezza in pagine del buffer Datatables** al valore iniziale, per non subire rallentamenti a livello di gestionale.
