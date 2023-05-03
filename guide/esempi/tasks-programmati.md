---
description: Come gestire le operazioni con OpenSTAManager
---

# 🗓 Tasks programmati

{% hint style="info" %}
E' possibile gestire le operazioni programmate in OpenSTAManager accedendo al database, dalla tabella zz\_tasks.
{% endhint %}

Le operazioni programmate di default sono:

* Backup: ogni giorno all'1.
* Importazione automatica ricevute FE: ogni 24 ore.
* Eliminazione automatica della coda d'invio: ogni 4 ore.

![](<../../.gitbook/assets/immagine (395).png>)

La determinazione del momento in cui verrà eseguita l'operazione viene determinata dall'espressione presente in Expression.&#x20;

Essa è determinata da cinque elementi combinati a caratteri speciali che indicano rispettivamente:

* minuto: 0 - 59
* ora: 0 - 23
* giorno (del mese): 1 - 31
* mese: 1 - 12
* giorno (della settimana): 0 - 6

I caratteri speciali che si possono trovare sono:

* \* -> qualsiasi valore
* , -> separatore di valori in una lista
* \- -> range di valori
* / -> intervallo di valori\


E' possibile verificare queste impostazioni in siti che verificano se la configurazione del cron è corretta come ad esempio: [https://crontab.guru/](https://crontab.guru/).

{% hint style="info" %}
**cron.php**: Script dedicato alla gestione delle operazioni di cron ricorrenti del gestionale.\
Una volta attivato, rimane in background per gestire l'esecuzione delle diverse operazioni come pianificate nella tabella zz\_tasks.
{% endhint %}

Il file viene richiamato in automatico al login di un utente.

Per garantire che lo script resti attivo in ogni situazione, si consiglia di introdurre una chiamata nel relativo crontab di sistema secondo il seguente schema:

Schema crontab: "/5 \* \* \* php \<percorso\_root>/cron.php"
