---
description: Come emettere un'autofattura con OpenSTAManager
metaLinks:
  alternates:
    - https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/guide/esempi/autofattura
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

### Scritture contabili

Le scritture contabili relative a questi movimenti risulteranno essere le seguenti:

![](<../../.gitbook/assets/image (735).png>)

I documenti che si riscontreranno al termine di questa operazione sono 3:

1. Fattura estera di acquisto
2. Autofattura registrata tra le fatture di vendita nel sezionale Autofatture
3. Autofattura registrata tra le fatture di acquisto nel sezionale Autofatture

### Registrazione fattura estera

Come primo passo si dovrà procede alla registrazione della fattura di acquisto estero ricevuta in via cartacea o all'importazione dallo SDI della fattura ricevuta con Reverse Charge

{% hint style="danger" %}
Questa fattura andrà registrata come la si riceve, non si deve quindi aggiungere manualmente l'IVA.
{% endhint %}

<figure><img src="../../.gitbook/assets/immagine (833).png" alt=""><figcaption></figcaption></figure>

In Tipo documento si dovrà scegliere la tipologia del documento corretta tra:

* **TD16** – **integrazione fattura per** **reverse charge interno**: da inviare in caso di ricevimento di fatture passive Italia soggette al regime di inversione contabile (art.17, commi 5 e 6 del DPR n. 633/1972 - art. 74 del DPR n.633/1972). Nella sezione 2.1.6 - Dati fatture collegate devono essere riportati gli estremi della fattura di riferimento; _» Reverse charge Italia_
* **TD17** – **integrazione/autofattura per** **acquisto servizi dall’estero**: da inviare in caso di ricevimento di fatture estere per acquisti di servizi territorialmente rilevanti ai fini IVA in Italia qualora il fornitore sia soggetto passivo stabilito ai fini IVA in altro Paese della UE o in un Paese extra-UE (art. 17 2 comma DPR 633/72); _» Servizi CEE e extraCEE_
* **TD18** – **integrazione per acquisto di beni intracomunitari**: da inviare in caso di ricevimento di fatture CEE per acquisti intracomunitari di beni (art. 38 del DL n. 331/1993); _» Beni CEE_
* **TD19** – **Integrazione/autofattura per acquisto di beni ex art. 17 c. 2 DPR n. 633/1972**: da inviare in caso di acquisti di beni territorialmente rilevanti in Italia, diversi dagli acquisti intracomunitari e dalle importazioni da soggetti non residenti (beni presenti in Italia); _» Beni extra CEE ma presenti in Italia_
* **TD 28 - Autofattura per acquisti da San Marino**

Una volta compilato il form si dovrà cliccare su Aggiungi, andare a selezionare la modalità di pagamento e procedere all'inserimento delle righe, per cui andrà selezionata una categoria IVA Non Imponibile.

<figure><img src="../../.gitbook/assets/immagine (747).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/immagine (555).png" alt=""><figcaption></figcaption></figure>

### Creazione autofattura di vendita

Cliccando sulla fattura appena registrata si accederà alla schermata di dettaglio della stessa, dove sarà possibile notare un avviso che guida alla generazione dell'autofattura per andare a reintegrare l'IVA, si dovrà quindi cliccare su Crea/Autofattura.

![](<../../.gitbook/assets/image (616).png>)

{% hint style="info" %}
Avviando questa procedura si può notare che si sta attualmente lavorando nel sezionale **Autofatture.**
{% endhint %}

![](<../../.gitbook/assets/image (460).png>)

Con **Crea autofattura** appariranno ora due avvisi: il riferimento alla fattura di acquisto originale, e l'avviso che si tratta di una fattura per conto terzi.

![](<../../.gitbook/assets/image (405).png>)

Andando ad analizzare le righe si potrà vedere l'IVA per integrazione presente in questo documento.

![](<../../.gitbook/assets/image (606).png>)

Le righe possono essere sintetizzate con i riferimenti alle normative in base al tipo di documento:

* "Autofattura Art.17, c.5-6 DPR 633/72" per **TD16**
* "Autofattura Art.17, c.2 DPR 633/72" per **TD17**&#x20;
* "Autofattura Art.38 del DL n. 331/1993" per **TD18**
* "Autofattura ex Art.17, c.2 DPR 633/72" per **TD19**

Questa fattura andrà ora emessa e inviata allo SDI.

### Importazione autofattura di acquisto

All'atto di importazione delle fatture di acquisto, dopo che sarà esaminata e approvata dallo SDI, si potrà trovare l'autofattura da importare che andrà a registrarsi nel sezionale Autofatture.

{% hint style="info" %}
Nel campo autofattura collegata si potrà selezionare l'autofattura di vendita da collegare.
{% endhint %}

![](<../../.gitbook/assets/image (396).png>)

### Piano dei conti

Si potrà vedere a questo punto un movimento in prima nota, creatosi per andare a compensare i conti dello stato patrimoniale.

![](<../../.gitbook/assets/immagine (752).png>)

Andando ad analizzare il piano dei conti sarà ora possibile notare solo il movimento della fattura di acquisto ricevuta inizialmente, ma tra i **Conti transitori** dello Stato patrimoniale saranno presenti i due movimenti IVA a pareggio.

![Dettaglio Conto economico](<../../.gitbook/assets/image (618).png>)

![Dettaglio Stato patrimoniale](<../../.gitbook/assets/image (164).png>)

![Dettaglio pareggio IVA tra i Conti transitori](<../../.gitbook/assets/image (372).png>)

La procedura di integrazione IVA è terminata.

### Nota di credito da fornitore estero

Per registrare una nota di credito da fornitore estero si dovrà eseguire la medesima procedura, mettendo segno negativo davanti agli importi delle righe.&#x20;

I passaggi saranno quindi i seguenti:

* Fattura di acquisto originale da fornitore estero con le righe con valore negativo
* Si andrà a generare l'autofattura (di vendita)che avrà quindi valori negativi, dal documento appena registrato
* Si andrà a importare l'autofattura (di acquisto) che avrà valore negativo.

### Videoguida

{% content-ref url="../videoguide/autofattura.md" %}
[autofattura.md](../videoguide/autofattura.md)
{% endcontent-ref %}
