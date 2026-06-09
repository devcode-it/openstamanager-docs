---
description: Guida al plugin Pianificazione fatturazione in OpenSTAManager
icon: plug
---

# Pianificazione fatturazione

{% hint style="info" %}
Il plugin **Pianificazione fatturazione** è un componente del modulo **Contratti** dedicato alla completa gestione della fatturazione dei contratti registrati.
{% endhint %}

Per pianificare la fatturazione di un contratto è necessario che si verifichino le seguenti condizioni:

* Deve riportare la data di accettazione e di conclusione
* Lo stato deve essere: In lavorazione, Fatturato, Pagato o Parzialmente fatturato

{% hint style="success" %}
Le righe devono riportare sotto la voce **quantità**, un numero pari al numero di rate che si andranno a creare, e come importo unitario deve essere inserito l'importo della singola rata.
{% endhint %}

{% hint style="warning" %}
Tutte le righe del contratto vengono convertite in righe generiche, rendendo impossibile risalire ad eventuali articoli utilizzati all'interno del contratto e pertanto non movimentano il magazzino.
{% endhint %}

## ● Creazione

Per procedere alla pianificazione della fatturazione si dovrà cliccare sul tasto Pianifica.

<figure><img src="../../../../../.gitbook/assets/immagine (121).png" alt=""><figcaption></figcaption></figure>

Si aprirà quindi una schermata in cui sarà possibile pianificare la fatturazione specificando la ricorrenza delle rate, ed eventualmente modificando i mesi in cui cadranno, cliccando sulla checkbox a lato. E' inoltre possibile impostare il Giorno di fatturazione tra: inizio mese, fine mese, e un giorno fisso selezionato.

<figure><img src="../../../../../.gitbook/assets/immagine (122).png" alt=""><figcaption></figcaption></figure>

La sezione **Righe** invece riporta una serie di variabili che è possibile utilizzare per personalizzare la descrizione delle righe che verranno riportate in fattura e permette di stabilire la quantità da inserire in ogni rata.

<figure><img src="../../../../../.gitbook/assets/immagine (123).png" alt=""><figcaption></figcaption></figure>

Avendo impostato da esempio 12 rate da 50€+IVA con scadenza mensile si dovrà quindi impostare 1 quantità a rata, per far in modo che vengano generate le seguenti fatture in bozza:

<figure><img src="../../../../../.gitbook/assets/immagine (124).png" alt=""><figcaption></figcaption></figure>

Andando a selezionare Crea fattura si potranno ora vedere nelle note i riferimenti della rata e del contratto e nella descrizione la riga e il periodo a cui la rata fa riferimento.

<figure><img src="../../../../../.gitbook/assets/immagine (125).png" alt=""><figcaption></figcaption></figure>

E' inoltre possibile scegliere se aggiungere le righe appena create a una fattura di vendita già presente in bozze dello stesso cliente, o se creare un nuovo documento.

Dopo aver aggiunto queste rate, saranno disponibili per la fatturazione in Dashboard, dal widget Rate contrattuali:

<figure><img src="../../../../../.gitbook/assets/immagine (1354).png" alt=""><figcaption></figcaption></figure>
