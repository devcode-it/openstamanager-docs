---
description: Guida al plugin Fatturazione Elettronica di OpenSTAManager.
icon: bolt
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/imnORsInuaaXiiRnlr6m/openstamanager/modules/acquisti/fatturediacquisto/fatturazione-elettronica
---

# Fatturazione Elettronica

Acquistando uno dei pacchetti OpenSTAManager con incluso l'invio e la ricezione delle fatture elettroniche si potrà gestire la propria fatturazione dal gestionale, dopo aver configurato la propria API key in Strumenti/Impostazioni/Fatturazione elettronica/OSMCloud Services API Token.

Con questo plugin è possibile importare nel gestionale le fatture elettroniche di acquisto scaricandole dal proprio cassetto fiscale. Le fatture da importare vengono visualizzate nella sezione inferiore della pagina, e tramite **Importa in sequenza** è possibile importarle massivamente.

<figure><img src="../../../../.gitbook/assets/immagine (71).png" alt=""><figcaption></figcaption></figure>

E' inoltre possibile caricare l'XML di una fattura di acquisto dalla sezione **Carica un XML**.

Dopo aver cliccato su **Importa** verrà caricata la seguente schermata:

<figure><img src="../../../../.gitbook/assets/immagine (72).png" alt=""><figcaption></figcaption></figure>

Andranno qui definite le specifiche della fattura da importare:

* Il tipo di documento
* Il sezionale in cui importare la fattura
* La data di registrazione della fattura
* La modalità di pagamento
* Se movimentare gli articoli presenti a magazzino
* Se creare automaticamente gli articoli non presenti a magazzino
* Se creare i seriali automaticamente per gli articoli caricati

In corrispondenza delle righe è possibile definire:

* Selezionare l'articolo corrispondente se presente a magazzino o eventualmente crearlo al volo
* Selezionare il conto acquisti
* Selezionare l'aliquota IVA

Cliccando su Altro è inoltre possibile stabilire:

* Se collegare un ordine di acquisto
* Se collegare un documento di vendita
* Se Aggiornare il prezzo di acquisto presente a magazzino e il relativo listino fornitore o se non apportare modifiche alla scheda articolo.

<figure><img src="../../../../.gitbook/assets/immagine (73).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/immagine (1382).png" alt=""><figcaption></figcaption></figure>

### Gestione dell'unità di misura secondaria

{% hint style="info" %}
Nel caso in cui nella scheda articolo sia impostata un'unità di misura secondaria con il corrispondente [fattore moltiplicativo](https://docs.openstamanager.com/v/2.4.44/openstamanager/modules/magazzino/articoli-1#fattore-moltiplicativo), in questa schermata verrà visualizzata l'unità di misura secondaria. L'articolo verrà invece caricato a magazzino per la corretta quantità e unità di misura primaria stabilite nella scheda articolo.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/immagine (968).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/immagine (524).png" alt=""><figcaption></figcaption></figure>

