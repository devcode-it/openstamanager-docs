---
description: >-
  Raccolta di errori frequenti nella compilazione di fatture elettroniche degli
  utenti OpenSTAManager
---

# ⛔ Errori frequenti

{% hint style="danger" %}
Utilizzare caratteri speciali
{% endhint %}

Di seguito sono riportati dei caratteri che spesso vengono utilizzati ma che non sono corretti nella compilazione di una **Fattura**:

* La **&** deve essere sostituita con **e**.
* Il simbolo **€** non deve essere presente. Si può utilizzare la parola **euro.**
* Non usare **%** e i trattini ( **- , \_** ).

{% hint style="danger" %}
Assenza di **dati obbligatori** nel documento
{% endhint %}

{% hint style="danger" %}
Duplicazione di fattura (stesso numero, stesso cedente/prestatore e anno)
{% endhint %}

{% hint style="danger" %}
Il file contiene una data antecedente ad un documento già inviato ad esso collegato (Esempio: si sta inviando una fattura del 01/03/2019 a cui è collegata una fattura di acconto o nota di credito del 10/03/2019)
{% endhint %}

{% hint style="danger" %}
Indicazione del **codice destinatario** in lettere minuscole. Il sistema lo riconosce solo quando è composto da lettere **MAIUSCOLE** e/o numeri in cifra
{% endhint %}

{% hint style="danger" %}
Se si vuole indicare un **codice IBAN** per ricevere i pagamenti (dato non obbligatorio), l'**IBAN** deve essere formalmente corretto
{% endhint %}

{% hint style="danger" %}
Mettere i caratteri rappresentate il paese nell'inserimento dell'**IVA**, selezionando la **nazione** il gestionale metterà in automatico i caratteri davanti alla partita **IVA.**
{% endhint %}

{% hint style="danger" %}
Quando si inserisce un **CAP** verificare che sia corretto, di 5 cifre, nel caso fosse un **CAP** estero il gestionale fa un controllo sulla **nazione** della anagrafica e se è minore di 5 cifre lo sostituisce con 5 zeri(00000)
{% endhint %}
