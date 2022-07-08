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

![](<../.gitbook/assets/image (47) (1) (1) (1) (1) (1).png>)

Come primo passo si dovrà procede alla registrazione della fattura di acquisto estero ricevuta in via cartacea o all'importazione dallo SDI della fattura ricevuta con Reverse Charge

{% hint style="danger" %}
Questa fattura andrà registrata come la si riceve, non si deve quindi aggiungere manualmente l'IVA.
{% endhint %}

![](<../.gitbook/assets/immagine (22).png>)

![](<../.gitbook/assets/immagine (48) (1).png>)

Cliccando sulla fattura appena registrata si accederà alla schermata di dettaglio della stessa, dove sarà possibile notare un avviso che guida alla generazione dell'autofattura per andare a reintegrare l'IVA, si dovrà quindi cliccare su Crea/Autofattura.

![](<../.gitbook/assets/immagine (50) (1) (1) (1).png>)

Si aprirà ora un menu che permetterà di scegliere la tipologia del documento corretta tra:

* **TD16** – integrazione fattura **reverse charge interno**;
* **TD17** – integrazione/autofattura per **acquisto servizi dall’estero** (prestazioni reste dal Cedente/Prestatore estero, anche residente nella Repubblica di San Marino o nello Stato della Città del Vaticano, nei confronti di un C/C residente o stabilito nel territorio nazionale);
* **TD18** – **integrazione/autofattura per acquisto beni intracomunitari** (vendita dal Cedente/Prestatore residente in altro paese UE di beni al C/C residente o stabilito nel territorio nazionale);
* **TD19** – **Integrazione/autofattura per acquisto di beni ex art.17 c.2 DPR 633/72** (vendita da Cedente/Prestatore estero di beni già presenti in Italia);

Avviando questa procedura si può notare che si sta attualmente lavorando nel sezionale **Autofatture**, che la procedura guidata selezionerà autonomamente.

![](<../.gitbook/assets/immagine (29).png>)

Con **Crea autofattura** appariranno ora due avvvisi: il riferimento alla fattura di acquisto originale, e l'avviso che si tratta di una fattura per conto terzi.

![](<../.gitbook/assets/immagine (52) (1).png>)

Andando ad analizzare le righe si potrà vedere l'IVA per integrazione presente in questo documento.

![](<../.gitbook/assets/immagine (27).png>)

All'atto di importazione delle fatture di acquisto si potrà ora trovare l'autofattura da importare, che andrà a registrarsi nel sezionale Autofatture.

![](<../.gitbook/assets/immagine (8) (1).png>)

Si potrà vedere a questo punto un movimento in prima nota, creatosi per andare a compensare i conti dello stato patrimoniale.

![](<../.gitbook/assets/immagine (21) (1) (1).png>)

Andando ad analizzare il piano dei conti sarà ora possibile notare solo il movimento della fattura di acquisto ricevuta inizialmente, ma tra i **Conti transitori** dello Stato patrimoniale saranno presenti i due movimenti IVA a pareggio.

![Dettaglio Conto economico](<../.gitbook/assets/image (38) (1) (1) (1) (1) (1).png>)

![Dettaglio Stato patrimoniale](<../.gitbook/assets/image (76) (1) (1) (1) (1).png>)

![Dettaglio pareggio IVA tra i Conti transitori](<../.gitbook/assets/image (96) (1) (1) (1) (1) (1) (1) (1) (1).png>)

La procedura di integrazione IVA è terminata.
