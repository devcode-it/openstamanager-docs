---
description: Guida al modulo aggiuntivo Distinta base in OpenSTAManager
---

# 📗 Distinta base

**Distinta base** è uno dei diversi moduli acquistabili da **OpenstaSTAManager.** Il modulo permette la gestione della distinta base permettendo il collegamento tra più articoli.

{% hint style="info" %}
[Clicca qui](https://shop.openstamanager.com/prodotto/distinta-base/) per procedere all'acquisto.
{% endhint %}

A seguito dell'installazione del modulo, navigando su **Magazzino->Articoli** e cliccando su un articolo apparirà alla destra la seguente schermata dei plugin disponibili.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2F0r5WwNOWmZRBFsmHmix2%2Ffile.png?alt=media)

![](<../.gitbook/assets/image (30).png>)

Tramite il pulsante + è possibile aggiungere articoli alla distinta:

![](<../.gitbook/assets/image (156).png>)

Dopo aver selezionato gli articoli che vanno a formare la distinta, è possibile movimentare correttamente il magazzino con i due tasti evidenziati:

* Produci: incrementa la quantità del prodotto finito e diminuisce la quantità degli articoli che servono a costruirlo
* Scomponi: diminuisce la quantità del prodotto finito e ripristina la quantità degli elementi che lo compongono.

![](<../.gitbook/assets/image (579).png>)

#### Produci articoli della distinta base in fase di vendita

Questa impostazione, se abilitata, permette l'esecuzione automatica dei meccanismi di composizione e scomposizione dell'articolo padre inserito in fattura, mantenendo bloccata la sua giacenza, e andando a movimentare invece le giacenze degli articoli figli.

Questa funzionalità è stata pensata per le attività che assemblano gli articoli padre al momento della vendita e non ne tengono delle quantitià fisse presenti a magazzino, come per esempio un negozio di informatica che vende un pc assemblato con dei specifici componenti. Al momento della vendita del pc assemblato non si andrà a ridurre la quantità dell'articolo padre _Computer_, ma andranno scalate a magazzino le quantità relative ai suoi componenti, mantenendo così allineate le giacenze.

Con questa impostazione abilitata si devono però tenere sotto controllo le giacenze degli articoli figli perchè in caso non siano sufficienti alla composizione dell'articolo padre inserito in fattura verranno comunque movimentati, e la loro giacenza assumerà quindi valore negativo.

Per automatizzare questo processo e avere il pieno controllo del magazzino non rischiando così di compromettere il flusso di lavoro a causa di materie prime mancanti, è stato sviluppato il modulo aggiuntivo [**Riordino fornitori**](riordino-fornitori.md), che permette di gestire in maniera ottimale la quanittà di materiale presente a magazzino, evidenziando gli articoli presenti in quantità inferiore alla soglia minima impostata e quelli presenti in quantità non sufficiente ad assolvere gli ordini cliente in cui sono impegnati, tenendo in considerazione gli articoli che fanno parte di una distinta base.

**Produci articoli della distinta base in fase di acquisto**

Questa impostazione, se abilitata, permette di scomporre un articolo importato da una fattura di acquisto negli articoli figli che compongono la distinta.

Esempio: Alla registrazione di una fattura di acquisto di una macchina, se l'impostazione è attiva, verrà simulata la produzioe della macchina e subito dopo la scomposizione nei singoli componenti, che verranno registrati a magazzino.
