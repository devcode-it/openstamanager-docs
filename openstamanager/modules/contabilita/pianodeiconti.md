---
description: Come gestire il Piano dei conti in OpenSTAManager
icon: circle
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/imnORsInuaaXiiRnlr6m/openstamanager/modules/contabilita/pianodeiconti
---

# Piano dei conti

{% hint style="info" %}
Da questo modulo è possibile visualizzare il piano dei conti, diviso in Conto economico e Stato patrimoniale.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (867).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
E' possibile visualizzare nel dettaglio gli elementi che lo compongono espandendo il menu a lato delle singole voci.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (868).png" alt=""><figcaption></figcaption></figure>

## Creazione

Per creare un nuovo conto si dovrà cliccare sul tasto (+) corrispondente alla voce sotto la quale si vorrà inserire:

<figure><img src="../../../.gitbook/assets/immagine (604).png" alt=""><figcaption></figcaption></figure>

Andranno qui inserite le informazioni relative al nuovo conto:

* Numero (è consigliato inserire un numero progressivo a quelli esistenti)
* Descrizione
* Percentuale deducibile

<figure><img src="../../../.gitbook/assets/image (869).png" alt=""><figcaption></figcaption></figure>

## Modifica

Per modificare un conto si deve cliccare sul tasto <img src="../../../.gitbook/assets/image (293).png" alt="" data-size="original">.

Da qui sarà possibile modificare:

* Numero
* Descrizione
* Utilizza come (Costo, Ricavo, Ricavo e Costo)

<figure><img src="../../../.gitbook/assets/image (870).png" alt=""><figcaption></figcaption></figure>

## Apertura e chiusura bilancio

Queste funzioni consentono di effettuare la Chiusura Contabile del vecchio anno e l’Apertura Contabile del nuovo, procedendo alla loro movimentazione automatica in prima nota.

Con la Chiusura contabile:

* Tutti i Conti Economici vengono azzerati e girati a Risultato di Esercizio;
* Tutti i Conti Patrimoniali attivi vengono sommati e girati a Bilancio di Chiusura;
* Tutti i Conti Patrimoniali passivi vengono sommati e girati a Bilancio di Chiusura;
* Il Bilancio di Chiusura viene pareggiato dal Risultato di Esercizio.

Con l'Apertura contabile:

* Tutti i Conti Patrimoniali attivi vengono aperti con saldo uguale a quello dell’anno precedente, e girati a Bilancio di Apertura.
* Tutti i Conti Patrimoniali passivi vengono aperti con saldo uguale a quello dell’anno precedente, e girati a Bilancio di Apertura.
* Il Bilancio di Apertura viene pareggiato dal Risultato di Esercizio.

I tasti "Apertura bilancio" e "Chiusura bilancio" presenteranno colore azzurro se durante l'anno corrente questi movimenti non sono ancora stati effettuati, mentre presenteranno colore bianco nel caso in cui le scritture relative all'apertura o chiusura siano già presenti a gestionale.

<figure><img src="../../../.gitbook/assets/immagine (820).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/immagine (599).png" alt=""><figcaption></figcaption></figure>

Per procedere ai movimenti di chiusura bilancio si dovrà quindi:

1. impostare il filtro calendario al 31/12 dell'anno di cui chiudere
2. andare in Contabilità/Piano dei conti
3. cliccare **Chiusura bilancio**

Per procedere ai movimenti di apertura bilancio si dovrà invece:

1. impostare il filtro calendario in Gennaio dell'anno di cui aprire i conti
2. andare in Contabilità/Piano dei conti
3. cliccare su **Apertura bilancio**

