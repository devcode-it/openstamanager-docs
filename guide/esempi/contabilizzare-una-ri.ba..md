---
description: Come contabilizzare una Ricevuta Bancaria con OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/guide/esempi/contabilizzare-una-ri.ba.
---

# 🗓️ Contabilizzare una Ri.Ba.

Per contabilizzare una Ri.Ba. è necessario registrare le seguenti scritture:

### Registrazione della fattura

Registrazione della fattura di vendita con pagamento tramite Ri.Ba. (scrittura registrata automaticamente al momento dell'emissione di una fattura di vendita)

```
Cliente a Ricavi merci c/to vendite                        100
```

### Contabilizzazione della Ri.Ba.

Per contabilizzare la ricevuta bancaria è necessario effettuare la seguente registrazione in prima nota:

```
Banca effetti all'incasso a Cliente                        100
```

{% hint style="info" %}
Consigliamo di effettuare questa registrazione dal modulo Prima nota e non tramite Registra contabile, per fare in modo che la scadenza rimanga aperta e non risulti già conclusa e Pagata.
{% endhint %}

### Accredito al dopo incasso

Nel caso in cui si scelga l'accredito sul conto corrente dopo l'incasso del credito da parte della banca (al netto delle relative commissioni) si effettuerà la seguente registrazione  in prima nota:

```
Banca C/C a Anticipo banca per Ri.Ba.                        100
Oneri bancari a Banca C/C                                     20
```

### Accredito salvo buon fine

In caso invece di accredito salvo buon fine, al momento della maturazione degli effetti si andrà a chiudere la registrazione cliccando su **Registra contabile** dalla fattura, e registrando le seguenti scritture al momento dell'anticipazione resa disponibile dalla banca sul conto corrente:

```
Banca C/C a Banca effetti all'incasso                        100
Oneri bancari a Banca C/C                                     20
```

Al momento dell'avvenuto incasso dalla banca dell'importo iscritto sulla ricevuta in oggetto si dovrà invece registrare:

```
Anticipo banca per Ri.Ba. a Banca effetti all'incasso        100
```

### Registrazione dell'insoluto

Nel caso di Ri.Ba. insoluta, si dovrà registrare la riapertura del conto cliente a fronte degli effetti all'incasso e la registrazione degli oneri bancari:

```
Cliente a Banca effetti all'incasso                            100
Spese insoluti a Banca C/C                                      30
```

{% hint style="info" %}
Nel caso di contabilizzazione della Ri.Ba. effettuata correttamente dal modulo Prima nota, sarà possibile aggiungere questa scrittura direttamente tramite Registra contabile dalla fattura. Nel caso invece in cui si sia registrata la contabilizzazione tramite registra contabile, questa scrittura andrà inserita manualmente dal modulo Prima nota.
{% endhint %}

