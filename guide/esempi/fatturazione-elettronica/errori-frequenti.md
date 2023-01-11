---
description: >-
  Raccolta di errori frequenti nella compilazione di fatture elettroniche degli
  utenti OpenSTAManager
---

# ⛔ Errori frequenti

{% hint style="danger" %}
Assenza di **dati obbligatori** nel documento
{% endhint %}

{% hint style="danger" %}
Indicazione del **codice destinatario** in lettere minuscole. Il sistema lo riconosce solo quando è composto da lettere **MAIUSCOLE** e/o numeri in cifra
{% endhint %}

{% hint style="danger" %}
Mettere i caratteri rappresentate il paese nell'inserimento della **Partita IVA**, selezionando la **nazione** il gestionale metterà in automatico i caratteri davanti alla **Partita** **IVA.**
{% endhint %}

{% hint style="danger" %}
Quando si inserisce un **CAP** verificare che sia corretto, di 5 cifre, nel caso fosse un **CAP** estero il gestionale fa un controllo sulla **nazione** della anagrafica e se è minore di 5 cifre lo sostituisce con 5 zeri(00000)
{% endhint %}

## **Come inserire la ritenuta d'acconto in fattura**

In fattura è possibile specificare la ritenuta d'acconto riga per riga durante l'inserimento o la modifica di una riga.

Se per alcuni clienti la ritenuta d'acconto deve essere sempre presente nei documenti, essa può essere impostata nell'anagrafica cliente, per cui verrà suggerita automaticamente all'inserimento delle righe nei documenti.

Per poter procedere alla corretta emissione di una fattura con ritenuta d'acconto si dovrà inoltre specificare la **Causale ritenuta d'acconto** in Impostazioni/Fatturazione elettronica, che andrà a compilare il campo \<CausalePagamento> in fattura elettronica.

<figure><img src="../../../.gitbook/assets/immagine (191).png" alt=""><figcaption></figcaption></figure>
