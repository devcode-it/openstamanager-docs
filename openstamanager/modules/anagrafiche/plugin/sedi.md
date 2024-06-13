---
description: Guida al plugin Sedi in OpenSTAManager
---

# 📍 Sedi aggiuntive

{% hint style="info" %}
Questo plugin è dedicato alla completa gestione di tutte le eventuali sedi delle anagrafiche registrate all'interno di OpenSTAManager.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/immagine (9) (1).png" alt=""><figcaption></figcaption></figure>

La schermata principale del plugin è strutturata secondo la tabella generale predefinita, presentando inoltre la possibilità di creare e modificare gli elementi attraverso strutture grafiche che si sovrappongono agli altri contenuti (_modal_).

### ➕ Creazione

La creazione di nuovi elementi segue il funzionamento standard del gestionale, necessitando il click sul pulsante apposito all'interno dell'intestazione del plugin.

Viene quindi reso possibile compilare tutte le informazioni di base relative alla nuova sede da creare:

* Nome sede
* Indirizzo
* Codice destinatario
* Città
* CAP
* Provincia
* Km
* Nazione
* [Zona](../zone.md)
* Cellulare
* Telefono
* Indirizzo email
* Opt-out per newsletter

<figure><img src="../../../../.gitbook/assets/immagine (12) (1).png" alt=""><figcaption></figcaption></figure>

### 🖌️ Modifica

La schermata di modifica, sebbene molto simile a quella di creazione, permette in particolare di impostare altre informazioni secondarie.

<figure><img src="../../../../.gitbook/assets/immagine (13) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Il **Codice destinatario** inserito in una determinata sede, verrà impostato come codice destinatario del cliente nei documenti di vendita in cui quella sede verrà selezionata.
{% endhint %}

Se l'impostazione [**Google Maps API key**](https://docs.openstamanager.com/modules/anagrafiche/modifica#geolocalizzazione) viene impostata, sarà possibile visualizzare la geolocalizzazione dall'interno dell'anagrafica.

{% hint style="warning" %}
La sede legale, predefinita per l'anagrafica, non viene registrata allo stesso modo delle altre sedi. Sarà pertanto impossibile eliminarla completamente da un'anagrafica.
{% endhint %}
