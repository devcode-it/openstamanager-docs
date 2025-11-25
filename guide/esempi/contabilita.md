---
description: Come gestire gli incassi e pagamenti con OpenSTAManager
metaLinks:
  alternates:
    - https://app.gitbook.com/s/WkbGuoumAhr6AzXH9lzV/guide/esempi/contabilita
---

# 💶 Incassi e pagamenti

Aprendo il modulo **Scadenzario** è possibile vedere le **Fatture di acquisto** e le **Fattura di vendita** che sono state emesse, suddivise per le scadenze relativamente registrate.

Indicate in rosso si potranno notare le fatture che hanno superato la data di scadenza.

![](<../../.gitbook/assets/image (758).png>)

#### Registrare il pagamento di una fattura

Per registrare il pagamento di una fattura è sufficiente aprire la fattura e cliccare sul tasto **Registra contabile**

<figure><img src="../../.gitbook/assets/immagine (1070).png" alt=""><figcaption></figcaption></figure>

Si aprirà quindi il modal precompilato da cui registrare il movimento in prima nota relativo al pagamento, cliccando su Aggiungi.

<figure><img src="../../.gitbook/assets/immagine (1071).png" alt=""><figcaption></figcaption></figure>

Sarà ora possibile visualizzare anche la seconda rata come pagata.

<figure><img src="../../.gitbook/assets/immagine (1072).png" alt=""><figcaption></figcaption></figure>

#### Esempio:&#x20;

Creando un **Fattura di vendita** e inserendo come pagamento **Bonifico 30/60/90/120gg** al momento della sua emissione nello scadenzario saranno generate quattro diverse scadenze.

Queste scadenze avranno la stessa data di emissione, riferimento fattura e importo, ma con data di scadenza diversa in base alla rata.

![](<../../.gitbook/assets/image (626).png>)

### Chiudere una fattura

Quando la **Fattura di vendita** è stata pagata dal cliente, per non visualizzarla più nello **Scadenzario** si possono adottare 2 metodi differenti:

* Con prima nota (Scopri come dal modulo [Prima nota](https://docs.openstamanager.com/modules/contabilita/primanota#creazione))
* Da scadenzario (Scopri come dal modulo [Scadenzario](https://docs.openstamanager.com/modules/contabilita/scadenzario#modifica))

Nello Scadenzario sono presenti sia le Fatture di acquisto che le Fatture di vendita. Le fatture con importo **positivo** sono **Fatture di vendita,** le fatture con importo **negativo** sono **Fatture di acquisto.**

Per tenere traccia dei pagamenti scaduti e da effettuare è necessario filtrare la ricerca andando ad inserire in **Data scadenza** mese e anno, nel seguente formato: mese/anno es. 02/2019.

Cosi' facendo sarà possibile vedere i pagamenti scaduti e da effettuare nel mese e anno selezionato. E' possibile filtrare i record inserendo anche solo l'anno 2018.

### Stampa

Il gestionale permette la stampa scadenzario dal tasto sotto alla tabella.

![](<../../.gitbook/assets/image (383).png>)

{% hint style="info" %}
Se si filtra la ricerca nello **Scadenzario** la stampa visualizzerà solo i record filtrati.
{% endhint %}
