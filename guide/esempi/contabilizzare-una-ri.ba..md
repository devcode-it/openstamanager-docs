---
description: Come contabilizzare una Ricevuta Bancaria con OpenSTAManager
---

# 🗓️ Contabilizzare una Ri.Ba.

Con OSM è possibile registrare correttamente una Ricevuta Bancaria e il relativo pagamento in 3 passaggi:

1. Registrazione della fattura di vendita con pagamento tramite Ri.Ba.

All'emissione del documento verrà generata la seguente scrittura:

```
Cliente a Ricavi merci c/to vendite
```

2. Al momento dell'emissione degli effetti da dentro la fattura si deve cliccare su Registra contabile e registrare le seguenti scritture:

```
Banca effetti all'incasso a Cliente
```

3. Al momento della maturazione degli effetti andrà riportato in prima nota:

```
Banca C/C a Banca effetti all'incasso
```

### Registrazione di una Ri.Ba. insoluta

```
Cliente a Banca effetti all'incasso
```
