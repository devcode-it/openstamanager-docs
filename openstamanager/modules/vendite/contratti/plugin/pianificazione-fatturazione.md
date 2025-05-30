---
description: Guida al plugin Pianificazione fatturazione in OpenSTAManager
---

# 📆 Pianificazione fatturazione

{% hint style="info" %}
Il plugin **Pianificazione fatturazione** è un componente del modulo **Contratti** dedicato alla completa gestione della fatturazione dei contratti registrati.
{% endhint %}

Per pianificare la fatturazione di un contratto è necessario che si verifichino le seguenti condizioni:

* Deve riportare la data di accettazione e di conclusione
* Lo stato deve essere: In lavorazione, Fatturato, Pagato o Parzialmente fatturato

{% hint style="success" %}
Le righe devono riportare sotto la voce **quantità**, un numero pari al numero di rate che si andranno a creare, e come importo unitario deve essere inserito l'importo della singola rata.
{% endhint %}

Esempio:

<figure><img src="../../../../../.gitbook/assets/immagine (318).png" alt=""><figcaption></figcaption></figure>

che a seguito della pianificazione fatturazione verranno convertite in:\


<figure><img src="../../../../../.gitbook/assets/immagine (553).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Tutte le righe del contratto vengono convertite in righe generiche, rendendo impossibile risalire ad eventuali articoli utilizzati all'interno del contratto e pertanto non movimentano il magazzino.
{% endhint %}

![](<../../../../../.gitbook/assets/image (185).png>)

## ➕ Creazione

Per procedere alla pianificazione della fatturazione si dovrà cliccare sul tasto Pianifica.

![](<../../../../../.gitbook/assets/immagine (311).png>)

Si aprirà quindi una schermata in cui sarà possibile pianificare la fatturazione specificando la ricorrenza delle rate, ed eventualmente modificando i mesi in cui cadranno, cliccando sulla checkbox a lato. E' inoltre possibile impostare il Giorno di fatturazione tra: inizio mese, fine mese, e un giorno fisso selezionato.

![](<../../../../../.gitbook/assets/immagine (405).png>)

La sezione **Righe** invece riporta una serie di variabili che è possibile utilizzare per personalizzare la descrizione delle righe che verranno riportate in fattura e permette di stabilire la quantità da inserire in ogni rata.

![](<../../../../../.gitbook/assets/immagine (397).png>)

Avendo impostato da esempio 4 rate da 200€+IVA con scadenza trimestrale si dovrà quindi impostare 1 quantità a rata, per far in modo che vengano generate le seguenti fatture in bozza:

![](<../../../../../.gitbook/assets/immagine (392).png>)

Andando a selezionare Crea fattura si potranno ora vedere nelle note i riferimenti della rata e del contratto e nella descrizione la riga e il periodo a cui la rata fa riferimento.

E' inoltre possibile scegliere se aggiungere le righe appena create a una fattura di vendita già presente in bozze dello stesso cliente, o se creare un nuovo documento.

![](<../../../../../.gitbook/assets/immagine (497).png>)
