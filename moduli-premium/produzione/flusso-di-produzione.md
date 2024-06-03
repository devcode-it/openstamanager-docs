---
description: Guida al Flusso di produzione in OpenSTAManager
---

# 🥽 Flusso di produzione

### Creazione della distinta base

E' possibile gestire la relazione tra articoli e materie prime tramite l'apposito plugin **Distinta base**:

{% content-ref url="../distinta-base.md" %}
[distinta-base.md](../distinta-base.md)
{% endcontent-ref %}

<figure><img src="../../.gitbook/assets/immagine (626).png" alt=""><figcaption></figcaption></figure>

### Creazione dell'ordine cliente

{% content-ref url="../../openstamanager/modules/vendite/ordinicliente/" %}
[ordinicliente](../../openstamanager/modules/vendite/ordinicliente/)
{% endcontent-ref %}

### Generazione ODL

Registrando un ordine cliente, sarà possibile inserire tra le righe l'articolo padre della distinta base appena creata.

Quando l'articolo verrà confermato si dovrà modificare la riga corrispondente, specificando la data prevista di evasione e confermando l'articolo.

<figure><img src="../../.gitbook/assets/immagine (640).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/immagine (130).png" alt=""><figcaption></figcaption></figure>

Dal modulo **Produzione/Genera ODL** si potrà ora visualizzare la riga corrispondente agli articoli da produrre per completare gli ordini, e tramite **Azioni di gruppo/Genera ODL** è possibile creare l'Odine di lavoro.

<figure><img src="../../.gitbook/assets/immagine (429).png" alt=""><figcaption></figcaption></figure>

### Modulo produzione

Dal modulo ODL sarà ora possibile visualizzare l'ODL:

<figure><img src="../../.gitbook/assets/immagine (460).png" alt=""><figcaption></figcaption></figure>

Entrando nell'ODL, sarà possibile visualizzare il dettaglio dell'Ordine di lavoro e delle rispettive fasi:

<figure><img src="../../.gitbook/assets/immagine (625).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/immagine (332).png" alt=""><figcaption></figcaption></figure>

### Materiale da acquistare

Da **Acquisti/Materiale da acquistare** è possibile visualizzare gli articoli da ordinare necessari alla produzione degli articoli padre di una distinta, gli articoli sottoscorta e le richieste di acquisto interne.

<figure><img src="../../.gitbook/assets/immagine (326).png" alt=""><figcaption></figcaption></figure>

Nell'ODL verrà ora visualizzata la quantità aggiornata

<figure><img src="../../.gitbook/assets/immagine (321).png" alt=""><figcaption></figcaption></figure>

In **Produzione** sarà ora possibile selezionare il reparto interessato e visualizzare la distribuzione del lavoro delle diverse settimane.

<figure><img src="../../.gitbook/assets/immagine (623).png" alt=""><figcaption></figcaption></figure>

Quando tutte le materie prime saranno disponibili a magazzino, a seguito quindi della registrazione di un ddt in entrata con il materiale mancante, la riga corrispondente alla fase da eseguire diventerà verde, e sarà possibile procedere all'esecuzione dell'ODL cliccando su Avanzamento:

<figure><img src="../../.gitbook/assets/immagine (678).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/immagine (458).png" alt=""><figcaption></figcaption></figure>

Al termine della lavorazione si dovrà cliccare su **Stop lavorazione,** e registrare la quantità prodotta.

<figure><img src="../../.gitbook/assets/immagine (627).png" alt=""><figcaption></figcaption></figure>

Dopo aver completato tutte le fasi della produzione dell'articolo, è possibile procedere all'invio della merce al cliente e alla sua fatturazione.

### Spedizione ordini

{% content-ref url="evasione-ordine.md" %}
[evasione-ordine.md](evasione-ordine.md)
{% endcontent-ref %}
