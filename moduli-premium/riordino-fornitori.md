---
description: Guida al modulo aggiuntivo Riordino fornitori in OpenSTAManager
---

# 📗 Riordino fornitori



{% hint style="info" %}
Il modulo **Riordino fornitori** permette di tenere sotto controllo le scorte di magazzino e ordinare le quantità di materiale corrette
{% endhint %}

### Funzionalità

#### Sezioni del Modulo

Il modulo presenta due sezioni principali:

**Articoli da ordinare**

Elenco degli articoli o di componenti facenti parte di una distinta base di un articolo impegnati in ordini clienti ma non disponibili a magazzino.

Il sistema calcola automaticamente:

* **Quantità necessaria**: calcolata sulla base delle quantità da evadere previste nelle righe degli Ordini cliente in stati Accettato e Parzialmente evaso
* **Quantità disponibile**: identificata dal magazzino articoli
* **Quantità ordinata**: ottenuta dalle quantità da evadere degli Ordini fornitore in stati Bozza, Accettato e Parzialmente evaso

**Articoli sottoscorta**

Elenco degli articoli presenti in quantità inferiore alla soglia minima impostata impegnati nei documenti di vendita o facenti parte della distinta di un articolo impegnato in un documento di vendita.

Per ogni articolo viene mostrata:

* **Quantità minima**: soglia minima impostata per l'articolo
* **Quantità a magazzino**: quantità attualmente disponibile nella sede selezionata
* **Quantità già ordinata**: quantità già ordinata ai fornitori ma non ancora ricevuta
* **Quantità da ordinare**: quantità suggerita per raggiungere la soglia minima

<figure><img src="../.gitbook/assets/immagine (363).png" alt=""><figcaption></figcaption></figure>

#### Filtri e Ordinamento

È possibile filtrare gli articoli in base a:

* **Fornitore**: selezionare un fornitore specifico per visualizzare solo gli articoli forniti da esso
* **Articolo**: cercare articoli specifici tramite il nome o codice
* **Sede destinazione**: selezionare la sede di destinazione per gli ordini fornitore

È possibile ordinare i fornitori in base a:

* **Prezzo più economico**: ordina i fornitori dal prezzo più basso al più alto
* **Prezzo più alto**: ordina i fornitori dal prezzo più alto al più basso
* **Tempi di consegna più rapidi**: ordina i fornitori per tempi di consegna più rapidi

{% hint style="warning" %}
Per visualizzare correttamente valorizzato il campo Fornitore, devono essere specificati i tempi di consegna dal plugin Listino fornitori dell'articolo interessato.
{% endhint %}

<figure><img src="../.gitbook/assets/immagine (364).png" alt=""><figcaption></figcaption></figure>

#### Gestione Quantità

Per ogni articolo è possibile:

* Selezionare l'articolo tramite checkbox
* Modificare la quantità da ordinare utilizzando i pulsanti +/- o inserendo direttamente il valore
* Visualizzare lo stato della quantità (quantità suggerita, deficit, eccesso)
* Selezionare il fornitore preferito tra quelli disponibili

#### Creazione Ordine Fornitore

Per procedere a creare un nuovo ordine fornitore:

1. Selezionare gli articoli interessati tramite i checkbox
2. Verificare le quantità da ordinare (modificabili se necessario)
3. Selezionare il fornitore per ogni articolo
4. Cliccare su **Crea ordine fornitore**
5. Confermare l'operazione cliccando su **Procedi**

Il sistema creerà automaticamente:

* Un ordine fornitore per ogni fornitore selezionato
* Le righe dell'ordine con i prezzi recuperati dal listino fornitore
* L'IVA del fornitore o quella predefinita del sistema

<figure><img src="../.gitbook/assets/immagine (365).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/immagine (366).png" alt=""><figcaption></figcaption></figure>

#### Visualizzazione Ordini Creati

Gli articoli appena ordinati non compariranno più tra gli articoli da ordinare o sottoscorta. Sarà possibile visualizzare l'ordine fornitore in:

* **Acquisti > Ordini fornitore** nel gestionale
* Direttamente dal modulo se è stato creato un solo ordine (redirect automatico)

<figure><img src="../.gitbook/assets/immagine (1181).png" alt=""><figcaption></figcaption></figure>

#### Scomposizione Distinta Base

Il modulo supporta la scomposizione automatica degli articoli tramite distinta base:

* Gli articoli composti vengono scomposti nei loro componenti
* Le quantità vengono calcolate in base alla composizione della distinta base
* Vengono mostrati solo i componenti effettivamente necessari

#### Gestione per Sede

Il modulo supporta la gestione delle scorte per sede:

* È possibile selezionare la sede di destinazione per gli ordini fornitore
* Le quantità disponibili vengono calcolate per sede specifica
* Le soglie minime possono essere impostate per sede

***

## Changelog

Tutti i maggiori cambiamenti di questo progetto saranno documentati in questo file. Per informazioni più dettagliate, consultare il log GIT della repository su GitHub.

Il formato utilizzato è basato sulle linee guida di [Keep a Changelog](http://keepachangelog.com/), e il progetto segue il [Semantic Versioning](http://semver.org/) per definire le versioni delle release.

* 4.0 (2026-03-17)
* 3.1 (2025-10-15)
* 3.0 (2025-07-22)
* 2.0 (2024-06-05)

### 4.0 (2026-03-17)

#### Aggiunto (Added)

* Aggiunto gulpfile.js per automazione build
* Aggiunto package.json per gestione dipendenze
* Aggiunto sistema di verifica integrità tramite file JSON (modules.php, settings.php, structure.php, views.php)

#### Modifiche

* Aggiornato .gitignore per escludere file di sistema e dipendenze

### 3.1 (2025-10-15)

#### Aggiunto (Added)

* Aggiunto filtro per sede su articoli da ordinare

### 3.0 (2025-07-22)

#### Aggiunto (Added)

* Aggiunta gestione riordino per sede

#### Modifiche

* Miglioria grafica modulo

#### Fix

* Allineamento modulo con spostamento threshold per sede

### 2.0 (2024-06-05)

#### Aggiunto (Added)

* Aggiunto php-cs-fixer
* Aggiunto rector

#### Modifiche

* Ottimizzato per compatibilità con php8.3
* Allineato a OSM 2.5.2
