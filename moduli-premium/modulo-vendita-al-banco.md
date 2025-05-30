---
description: Guida al modulo aggiuntivo Vendita al banco in OpenSTAManager
---

# 📗 Vendita al banco

**Vendita al banco** è uno dei diversi moduli acquistabili da **OpenSTAManager.** Il modulo permette la vendita al banco di prodotti con o senza codice a barre.

{% hint style="info" %}
[Clicca qui](https://shop.openstamanager.com/prodotto/vendita-al-banco/) per procedere all'acquisto
{% endhint %}

Di seguito sono elencati i parametri consigliati per il registratore di cassa:

* PARAMETRI COMUNICAZIONE PROTOCOLLO: **XON/XOFF**
* BAUNDRATE: **9600**
* BIT NUMBER: **\[8,NONE,1]**
* XON-XOFF TX FOOTER: **\[DISABILITATO]**
* XON-XOFF TX ECO: **\[DISABILITATO]**
* HANDSHAKE: **\[XON/XOFF]**
* MODO FPU: **\[DISABILITATO]**
* CANALE PC: **\[Ethernet]**
* VIRGOLA INCLUSA: **SI**
* ECHO FULL: **NO**

### 🔍 Requisiti

Compatibile con stampanti fiscali che supportano il protocollo xon-xoff e lavorano in rete.

## 🪙 Vendita al banco

A seguito dell'installazione del modulo, cliccando su **Vendita al banco** apparirà la seguente schermata:

<figure><img src="../.gitbook/assets/immagine (217).png" alt=""><figcaption></figcaption></figure>

### ➕ Creazione

Per creare una vendita al banco in OpenSTAManager si dovrà cliccare sul tasto (+).

La schermata che si presenterà sarà questa, dove sarà possibile inserire:

* Stato
* Magazzino
* Pagamento
* Cliente
* Agente
* Registratore di cassa
* Importo pagato
* Note
* Righe

<figure><img src="../.gitbook/assets/immagine (218).png" alt=""><figcaption></figcaption></figure>

Dopo aver inserito le righe interessate si dovrà cliccare su Chiudi vendita per concludere la vendita e registrare il pagamento.

### 🖌️ Modifica

Per poter modificare una vendita al banco chiusa, sarà necessario entrare nella vendita interessata e cliccare su Riapri vendita. Da qui sarà possibile apportare le modifiche necessarie.

<figure><img src="../.gitbook/assets/immagine (219).png" alt=""><figcaption></figcaption></figure>

## 💳 Easy vendita

Dal modulo Easy vendita invece si avrà l'interfaccia di un registratore di cassa, da cui sarà possibile movimentare i prodotti mediante scansione del codice a barre o selezionandoli dalle categorie presenti in magazzino.

I prodotti così inseriti si vedranno nella colonna di destra, dove sarà possibile modificarne le quantità, modificare la riga o toglierli dal carrello.

<figure><img src="../.gitbook/assets/immagine (222).png" alt=""><figcaption></figcaption></figure>

Cliccando su modifica riga si accederà alla seguente schermata, dove sarà possibile applicare uno sconto, cambiare l'aliquota IVA, il prezzo di acquisto e di vendita.

<figure><img src="../.gitbook/assets/immagine (223).png" alt=""><figcaption></figcaption></figure>

Una volta inseriti tutti i prodotti, sarà sufficiente cliccare il tasto PAGA e da qui sarà possibile chiudere il documento, procedere al pagamento e stamparne lo scontrino.

Cliccando il pulsante **Chiusura** sarà inoltre possibile selezionare il registratore di cassa da cui stampare lo scontrino, tramite l'apposito menu a tendina. Come valore di default viene selezionato il registratore collegato alla sede dell'utente che ha effettuato l'accesso nel caso in cui si tratti della prima vendita, dalla seconda vendita in poi viene invece selezionato automaticamente sempre l'ultimo registratore di cassa utilizzato.

Per modificare la vendita appena conclusa sarà necessario cliccare su Riapertura. Da qui sarà possibile apportare le modifiche necessarie.

<figure><img src="../.gitbook/assets/immagine (224).png" alt=""><figcaption></figcaption></figure>

## 💵 Tipologia pagamenti

Nel modulo **Tipologia pagamenti** è possibile specificare che tipologia di pagamento associare a una tipologia pagamenti corrispondente a un determinato codice configurato come da impostazioni del proprio registratore di cassa.

<figure><img src="../.gitbook/assets/immagine (225).png" alt=""><figcaption></figcaption></figure>

## 🗄️ Reparti

Nel modulo **Reparti** è possibile specificare i codici reparto da associare ai vari reparti, configurandoli come da impostazioni del proprio registratore di cassa.

<figure><img src="../.gitbook/assets/immagine (226).png" alt=""><figcaption></figcaption></figure>

## 💹 Statistiche vendite

In questo modulo è possibile visualizzare le statistiche delle vendite al banco effettuate, con l'esploso delle righe.

<figure><img src="../.gitbook/assets/immagine (227).png" alt=""><figcaption></figcaption></figure>

## 🧰 Registratori di cassa

Da questo modulo è possibile configurare i registratori di cassa da associare al gestionale, per utilizzarli durante la vendita al banco.

<figure><img src="../.gitbook/assets/immagine (228).png" alt=""><figcaption></figcaption></figure>
