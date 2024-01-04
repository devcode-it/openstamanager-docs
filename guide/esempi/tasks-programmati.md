---
description: Come gestire le operazioni con OpenSTAManager
---

# 🗓 Tasks programmati

{% hint style="info" %}
In OpenSTAManager è stato introdotto il modulo **Gestione Task** per modificare le azioni programmate definite a database in zz\_tasks
{% endhint %}

{% content-ref url="../../openstamanager/modules/strumenti/gestione-task.md" %}
[gestione-task.md](../../openstamanager/modules/strumenti/gestione-task.md)
{% endcontent-ref %}

![](<../../.gitbook/assets/immagine (648).png>)

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
