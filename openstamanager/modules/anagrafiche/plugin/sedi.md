---
description: Guida al plugin Sedi in OpenSTAManager
---

# 📍 Sedi

{% hint style="info" %}
Questo plugin è dedicato alla completa gestione di tutte le eventuali sedi delle anagrafiche registrate all'interno di OpenSTAManager.
{% endhint %}

![](<../../../../.gitbook/assets/image (598).png>)

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

![](<../../../../.gitbook/assets/image (495).png>)

### 🖌️ Modifica

La schermata di modifica, sebbene molto simile a quella di creazione, permette in particolare di impostare altre informazioni secondarie.

![](<../../../../.gitbook/assets/image (602).png>)

Se l'impostazione [**Google Maps API key**](https://docs.openstamanager.com/modules/anagrafiche/modifica#geolocalizzazione) viene impostata, sarà possibile visualizzare la geolocalizzazione dall'interno dell'anagrafica.

{% hint style="warning" %}
La sede legale, predefinita per l'anagrafica, non viene registrata allo stesso modo delle altre sedi. Sarà pertanto impossibile eliminarla completamente da un'anagrafica.
{% endhint %}
