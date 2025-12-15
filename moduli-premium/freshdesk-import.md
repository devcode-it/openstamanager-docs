---
description: Guida al modulo Freshdesk Import in OpenSTAManager
---

# 📗 Freshdesk Import

{% hint style="info" %}
Freshdesk import è un modulo che permette di importare i ticket da Freshdesk in OpenSTAManager, associandoli alle attività.
{% endhint %}

<figure><img src="../.gitbook/assets/immagine (1434).png" alt=""><figcaption></figcaption></figure>

### Funzionalità

* Visualizzazione dei ticket Freshdesk non ancora importati
* Associazione di ticket a attività esistenti
* Creazione di nuove attività a partire dai ticket
* Tagging automatico dei ticket importati su Freshdesk
* Visualizzazione dei dettagli del ticket all'interno dell'attività

### Configurazione

Per utilizzare il modulo è necessario configurare le seguenti impostazioni:

1. **Freshdesk API Key**: La chiave API per accedere a Freshdesk
2. **Freshdesk Domain**: Il dominio Freshdesk (es. azienda.freshdesk.com)
3. **Freshdesk Import Tag**: Il tag da aggiungere ai ticket importati (default: imported\_to\_osm)

Queste impostazioni possono essere configurate direttamente nel modulo.

### Utilizzo

1. Accedere al modulo "Importa Ticket Freshdesk" dal menu Strumenti
2. Configurare le impostazioni di Freshdesk se non ancora fatto
3. Selezionare un cliente per ogni ticket da importare
4. Opzionalmente, selezionare un'attività esistente a cui collegare il ticket
5. Cliccare sul pulsante "Collega" per associare il ticket all'attività selezionata o per creare una nuova attività

Una volta importato, il ticket sarà visibile nella scheda "Ticket Freshdesk" dell'attività associata.
