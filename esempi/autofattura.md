# Autofattura

{% hint style="info" %}
Come emettere un'**Autofattura**
{% endhint %}

In seguito alla ricezione di una fattura in Reverse Charge o di una fattura estera vi è la necessità di emettere un'autofattura per integrare l'IVA a nostro carico.&#x20;

La **Manovra 2021** (_legge 178/2020)_ precisa **i termini per l’emissione** dei file XML relativi alle operazioni transfrontaliere:

{% hint style="info" %}
Le **fatture attive** dovranno essere emesse verso soggetti esteri _entro 12 giorni dall’effettuazione_ _dell’operazione_ oppure _entro il giorno 15 del mese successivo_ a quello a cui si riferiscono le operazioni riportate in fattura, se si tratta di fattura elettronica differita
{% endhint %}

{% hint style="info" %}
Le **fatture passive** ricevute da soggetti esteri andranno integrate _entro il giorno 15 del mese successivo_ a quello in cui sono stati ricevuti i documenti che provano l’effettuazione dell’operazione.
{% endhint %}

Le scritture contabili relative a questi movimenti risulteranno essere le seguenti:

![](<../.gitbook/assets/image (47).png>)

In **OpenSTAManager** per poter procedere all'emissione di un'autofattura è consigliato seguire prima alcuni passaggi:

Per prima cosa si deve andare a modificare il tipo di anagrafica della propria azienda aggiungendovi il tipo "Fornitore" e quella dei fornitori che ci invieranno fatture in Reverse Charge aggiungendo la tipologia "Cliente". Per fare ciò si dovrà quindi accedere alla sezione "Informazioni aggiuntive" delle anagrafiche interessate e andare a inserirle manualmente.

![Modifica tipo anagrafica](<../.gitbook/assets/immagine (12).png>)

Per far si che le registrazioni contabili risultino normalizzate si dovrà poi creare un apposito conto in cui far confluire i costi e ricavi generati. Per creare un nuovo conto dello stato patrimoniale si deve premere sul tasto **(+)**, aggiungere una nuova categoria (**Conti Compensativi**), e selezionare Utilizza come **Ricavo e Costo**.

![](<../.gitbook/assets/immagine (15).png>)

![Creazione nuova tipologia di conto ](<../.gitbook/assets/immagine (24).png>)

Ora si dovrà creare il conto "Compensazione per autofattura" che si andrà ad utilizzare al momento della registrazione dell'autofattura in entrata e uscita.

![Creazione nuovo conto](<../.gitbook/assets/immagine (27).png>)

Come ultimo passo in preparazione all'emissione di autofatture è consigliato creare due appositi **Sezionali** in cui raggrupparle, uno per le fatture di vendita e uno per quelle di acquisto, da Strumenti/Segmenti premendo il tasto **Aggiungi (+)**.

Qui si dovranno inserire il Nome e il modulo a cui i nostri sezionali dovranno riferirsi.

![Creazione sezionale](<../.gitbook/assets/immagine (18).png>)

Si registrerà ora la fattura di acquisto estero ricevuta in via cartacea o importando dal SDI la fattura ricevuta con Reverse Charge.&#x20;

![Registrazione fattura di acquisto](<../.gitbook/assets/immagine (7).png>)

![](<../.gitbook/assets/immagine (14).png>)

Si potrà ora procedere ad emettere l'autofattura creando una nuova [Fattura di vendita](../modules/vendite/fatturedivendita/creazionefatturevendita.md) nel sezionale Autofatture, selezionando come Cliente il fornitore emittente la fattura di acquisto ricevuta, e come tipo di documento si dovrà scegliere tra:

* **TD16** – integrazione fattura **reverse charge interno**;
* **TD17** – integrazione/autofattura per **acquisto servizi dall’estero** (prestazioni reste dal Cedente/Prestatore estero, anche residente nella Repubblica di San Marino o nello Stato della Città del Vaticano, nei confronti di un C/C residente o stabilito nel territorio nazionale);
* **TD18** – **integrazione/autofattura per acquisto beni intracomunitari** (vendita dal Cedente/Prestatore residente in altro paese UE di beni al C/C residente o stabilito nel territorio nazionale);
* **TD19** – **Integrazione/autofattura per acquisto di beni ex art.17 c.2 DPR 633/72** (vendita da Cedente/Prestatore estero di beni già presenti in Italia);

![Creazione fattura di vendita per autofattura](<../.gitbook/assets/immagine (20).png>)

Si dovrà ora attivare la spunta su Fattura per conto terzi, andando così a invertire cliente e fornitore.

![Modifica fattura di vendita in fattura Reverse Charge](<../.gitbook/assets/immagine (3).png>)

All'atto dell'inserimento righe si andranno a selezionare il conto creato precedentemente e l'aliquota IVA adeguata da applicare.

![](<../.gitbook/assets/immagine (6).png>)

Tra le fatture di vendita nel sezionale Autofatture sarà ora possibile vedere la fattura appena creata e andando a esaminare l'XML del documento si troveranno cliente e fornitore nella giusta posizione.

![XML Reverse Charge](<../.gitbook/assets/immagine (8).png>)

Si dovrà ora registrare questa fattura tra quelle di acquisto, inserendo gli stessi valori della fattura di vendita appena emessa.

![Creazione fattura di acquisto per autofattura](<../.gitbook/assets/image (32).png>)

![](<../.gitbook/assets/image (46).png>)

Per normalizzare i valori dello stato patrimoniale si dovrà ora andare a eseguire un movimento in prima nota che avrà in Avere il conto utilizzato per il cliente della fattura di vendita (in questo caso è il conto Forniture impianti srl avendo fatto un'operazione con Reverse Charge, come lo si distingue dal codice rientrante tra quello dei Crediti clienti), e in Dare il conto utilizzato per il fornitore della fattura di acquisto appena registrata.

![Normalizzazione dei conti per compensazione](<../.gitbook/assets/image (81).png>)

Andando ad analizzare il piano dei conti sarà ora possibile trovarvi solo il movimento della fattura di acquisto ricevuta inizialmente, ma tra i **Conti transitori** dello Stato patrimoniale saranno presenti i due movimenti IVA a pareggio.

![Dettaglio Conto economico](<../.gitbook/assets/image (38).png>)

![Dettaglio Stato patrimoniale](<../.gitbook/assets/image (76).png>)

![Dettaglio pareggio IVA tra i Conti transitori](<../.gitbook/assets/image (96).png>)

