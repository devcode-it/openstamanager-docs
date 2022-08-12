# Gestione acconto

{% hint style="info" %}
Gestione degli acconti nei documenti di vendita.
{% endhint %}

Esempio: _Registrazione di un preventivo per un importo di 1000€ con acconto di 300€ e successivo saldo pari a 700€_

Creare un **preventivo** e inserire le seguenti righe:

1. Una o più righe per un importo pari ai **1000€**
2. Una riga con importo pari a **300€** che fa riferimento all'**acconto**
3. Una riga con importo pari a **-300€** che fa riferimento alla **detrazione** dell'acconto

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2F2lSsh5b757dplX4NwfQq%2Ffile.png?alt=media)

Successivamente creare una **fattura** **di** **vendita** importando la riga dell'acconto con l'importo di **300€** dal preventivo.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FaNmQRSKdjlryuALtcqDK%2Ffile.png?alt=media)

Infine creare una nuova **fattura** importando le **due** righe rimaste:

1. Riga del preventivo con l'importo totale del preventivo pari a **1000€**
2. Riga del preventivo con l'importo pari a **-300€** che fa riferimento alla detrazione dell'acconto

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2F16XFmEWcSiIwPnivQO67%2Ffile.png?alt=media)
