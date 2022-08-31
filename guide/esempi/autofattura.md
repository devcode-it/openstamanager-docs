---
description: Come emettere un'autofattura con OpenSTAManager
---

# 👏 Autofattura

In seguito alla ricezione di una fattura in Reverse Charge o di una fattura estera vi è la necessità di emettere un'autofattura per integrare l'IVA a nostro carico.

La **Manovra 2021** (_legge 178/2020)_ precisa **i termini per l’emissione** dei file XML relativi alle operazioni transfrontaliere:

{% hint style="info" %}
Le **fatture attive** dovranno essere emesse verso soggetti esteri _entro 12 giorni dall’effettuazione_ _dell’operazione_ oppure _entro il giorno 15 del mese successivo_ a quello a cui si riferiscono le operazioni riportate in fattura, se si tratta di fattura elettronica differita;
{% endhint %}

{% hint style="info" %}
Le **fatture passive** ricevute da soggetti esteri andranno integrate _entro il giorno 15 del mese successivo_ a quello in cui sono stati ricevuti i documenti che provano l’effettuazione dell’operazione.
{% endhint %}

Le scritture contabili relative a questi movimenti risulteranno essere le seguenti:

![](<../../.gitbook/assets/image (290).png>)

Come primo passo si dovrà procede alla registrazione della fattura di acquisto estero ricevuta in via cartacea o all'importazione dallo SDI della fattura ricevuta con Reverse Charge

{% hint style="danger" %}
Questa fattura andrà registrata come la si riceve, non si deve quindi aggiungere manualmente l'IVA.
{% endhint %}

![](<../../.gitbook/assets/image (635).png>)

![](<../../.gitbook/assets/image (630).png>)

Cliccando sulla fattura appena registrata si accederà alla schermata di dettaglio della stessa, dove sarà possibile notare un avviso che guida alla generazione dell'autofattura per andare a reintegrare l'IVA, si dovrà quindi cliccare su Crea/Autofattura.

![](<../../.gitbook/assets/image (643).png>)

Si aprirà ora un menu che permetterà di scegliere la tipologia del documento corretta tra:

* **TD16** – integrazione fattura per **reverse charge interno**: da inviare in caso di ricevimento di fatture passive Italia soggette al regime di inversione contabile (art.17, commi 5 e 6 del DPR n. 633/1972 - art. 74 del DPR n.633/1972). Nella sezione 2.1.6 - Dati fatture collegate devono essere riportati gli estremi della fattura di riferimento; -> Reverse charge Italia
* **TD17** – integrazione/autofattura per **acquisto servizi dall’estero**: da inviare in caso di ricevimento di fatture estere per acquisti di servizi territorialmente rilevanti ai fini IVA in Italia qualora il fornitore sia soggetto passivo stabilito ai fini IVA in altro Paese della UE o in un Paese extra-UE (art. 17 2 comma DPR 633/72); -> Servizi CEE e extraCEE
* **TD18** – integrazione per **acquisto di beni intracomunitari**: da inviare in caso di ricevimento di fatture CEE per acquisti intracomunitari di beni (art. 38 del DL n. 331/1993); -> Beni CEE
* **TD19** – Integrazione/autofattura per **acquisto di beni ex art. 17 c. 2 DPR n. 633/1972**: da inviare in caso di acquisti di beni territorialmente rilevanti in Italia, diversi dagli acquisti intracomunitari e dalle importazioni da soggetti non residenti (beni presenti in Italia); -> Beni extra CEE ma presenti in Italia

Avviando questa procedura si può notare che si sta attualmente lavorando nel sezionale **Autofatture**, che la procedura guidata selezionerà autonomamente.

![](<../../.gitbook/assets/image (634).png>)

Con **Crea autofattura** appariranno ora due avvisi: il riferimento alla fattura di acquisto originale, e l'avviso che si tratta di una fattura per conto terzi.

![](<../../.gitbook/assets/image (597).png>)

Andando ad analizzare le righe si potrà vedere l'IVA per integrazione presente in questo documento.

![](<../../.gitbook/assets/image (622).png>)

All'atto di importazione delle fatture di acquisto si potrà ora trovare l'autofattura da importare, che andrà a registrarsi nel sezionale Autofatture.

{% hint style="info" %}
Nel campo autofattura collegata si potrà selezionare l'autofattura di vendita da collegare.
{% endhint %}

![](<../../.gitbook/assets/image (600).png>)

Si potrà vedere a questo punto un movimento in prima nota, creatosi per andare a compensare i conti dello stato patrimoniale.

![](<../../.gitbook/assets/immagine (4).png>)

Andando ad analizzare il piano dei conti sarà ora possibile notare solo il movimento della fattura di acquisto ricevuta inizialmente, ma tra i **Conti transitori** dello Stato patrimoniale saranno presenti i due movimenti IVA a pareggio.

![Dettaglio Conto economico](<../../.gitbook/assets/image (299).png>)

![Dettaglio Stato patrimoniale](<../../.gitbook/assets/image (293).png>)

![Dettaglio pareggio IVA tra i Conti transitori](<../../.gitbook/assets/image (289).png>)

La procedura di integrazione IVA è terminata.

### ➖ Nota di credito da fornitore estero

Per registrare una nota di credito da fornitore estero si dovrà eseguire la medesima procedura, mettendo segno negativo davanti agli importi delle righe.&#x20;

I passaggi saranno quindi i seguenti:

* Fattura di acquisto originale da fornitore estero con le righe con valore negativo
* Si andrà a generare l'autofattura (di vendita)che avrà quindi valori negativi, dal documento appena registrato
* Si andrà a importare l'autofattura (di acquisto) che avrà valore negativo.
