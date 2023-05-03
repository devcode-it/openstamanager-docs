---
description: Come gestire le Fatture di vendita in OpenSTAManager
---

# 📃 Fatture di vendita

{% hint style="info" %}
Il modulo **Fatture di vendita** permette di gestire la fatturazione in uscita dell'azienda.
{% endhint %}

![](<../../../../.gitbook/assets/immagine (55).png>)

## ⚠️ Avvisi

Nel caso siano presenti delle fatture di vendita **generate** ma non ancora inviate (entro i 12 giorni dalla scadenza per inviare le fatture allo SDI), verranno segnalate dal gestionale con un avviso nella sezione fatture di vendita.

![](<../../../../.gitbook/assets/immagine (288).png>)

Verranno notificare anche le fatture che invece risulteranno **scartate** dallo SDI e andranno quindi corrette e riemesse.

![](<../../../../.gitbook/assets/immagine (206).png>)

## ➕ Creazione

Per creare una nuova Fattura di vendita si dovrà cliccare sul tasto (+).

Andranno qui inserite le informazioni relative alla nuova fattura di vendita:

* Data
* Cliente
* Tipo documento
* Sezionale

<figure><img src="../../../../.gitbook/assets/immagine (394).png" alt=""><figcaption></figcaption></figure>

## 🖌️ Modifica

Cliccando sul record da modificare si aprirà la schermata di dettaglio, da cui sarà possibile modificare:

* Numero fattura
* Data emissione
* Data competenza
* Stato FE
* Stato
* Cliente
* Agente di riferimento
* Referente
* Partenza merce
* Destinazione merce
* Tipo documento
* Pagamento
* Banca azienda
* Abilitare split payment
* Abilitare fattura per conto terzi
* Sconto in fattura ([Decreto Rilancio 2020](../../../../guide/esempi/fatturazione-elettronica/decreto-rilancio-2020.md))
* Ritenuta previdenziale
* Dichiarazione d'intento
* Abilitare marca da bollo automatica ([https://www.agenziaentrate.gov.it/portale/documents/20143/3394067/L%27imposta\_di\_Bollo\_sulle\_fatture\_elettronche.pdf/234d3993-fb09-2fd2-dbb9-7cc1dc0e799b](https://www.agenziaentrate.gov.it/portale/documents/20143/3394067/L'imposta\_di\_Bollo\_sulle\_fatture\_elettronche.pdf/234d3993-fb09-2fd2-dbb9-7cc1dc0e799b))
* Note
* Note interne

![](<../../../../.gitbook/assets/immagine (49) (1).png>)

* Righe, che possono includere:
  * Articolo
  * Riga generica
  * Descrizione
  * Sconto/maggiorazione
  * Attività
  * Preventivo
  * Contratto
  * DDT
  * Ordine
* Allegati

<figure><img src="../../../../.gitbook/assets/immagine (424).png" alt=""><figcaption></figcaption></figure>

### ✅ Operazioni massive sulle righe

E' possibile intervenire massivamente sulle righe dei documenti selezionandole e ricorrendo alle azioni di gruppo:

<figure><img src="../../../../.gitbook/assets/immagine (25).png" alt=""><figcaption></figcaption></figure>

* Duplica
* Elimina
* Confronta prezzi

#### Confronta prezzi

Tramite questa funzione è possibile visualizzare il prezzo utilizzato per gli articoli selezionati nell'ultimo documento e preventivo di vendita. Da qui è possibile modificare il prezzo di vendita massivamente cliccando su **Modifica**.

<figure><img src="../../../../.gitbook/assets/immagine (6).png" alt=""><figcaption></figcaption></figure>



## 🔧 Plugin

Selezionando uno specifico record si può accedere a diversi plugin nella barra laterale della pagina:

* Fatturazione elettronica
* Movimenti contabili
* Registrazioni
* Note interne
* Info

Dalla schermata del modulo è invece possibile accedere al plugin [RicevuteFE](ricevutefe.md).



## 🔽 Informazioni aggiuntive

{% content-ref url="plugin.md" %}
[plugin.md](plugin.md)
{% endcontent-ref %}

{% content-ref url="plugin-1/" %}
[plugin-1](plugin-1/)
{% endcontent-ref %}

{% content-ref url="../../../../guide/esempi/autofattura.md" %}
[autofattura.md](../../../../guide/esempi/autofattura.md)
{% endcontent-ref %}

{% content-ref url="../../../../guide/esempi/gestione-acconto.md" %}
[gestione-acconto.md](../../../../guide/esempi/gestione-acconto.md)
{% endcontent-ref %}

{% content-ref url="../../../../guide/esempi/nota-di-credito.md" %}
[nota-di-credito.md](../../../../guide/esempi/nota-di-credito.md)
{% endcontent-ref %}

{% content-ref url="../../../../guide/esempi/prezzo-di-vendita-automatico.md" %}
[prezzo-di-vendita-automatico.md](../../../../guide/esempi/prezzo-di-vendita-automatico.md)
{% endcontent-ref %}

{% content-ref url="../../../../guide/esempi/sconto-combinato.md" %}
[sconto-combinato.md](../../../../guide/esempi/sconto-combinato.md)
{% endcontent-ref %}
