# Contabilità

## Incassi e pagamenti

{% hint style="info" %}
Come tenere traccia dei pagamenti scaduti e da effettuare? 
{% endhint %}

Utilizzando il modulo **Scadenzario** è possibile tenere traccia dei pagamenti scaduti e da effettuare. 

Il ****modulo **Scadenzario** è presente sotto la voce **Contabilità** nel menu laterale di OpenSTAManager.

![](../.gitbook/assets/scadenzario.png)

Cliccandoci sopra è possibile vedere nella parte destra le **Fatture di acquisto** e le **Fattura di vendita** in stato di **Emessa.**

![](../.gitbook/assets/scadenzario1.png)

Esempio: creo un **Fattura di vendita** inserendo come pagamento **Bonifico 30/60/90/120gg d.f.** mettendola in stato di **Emessa,** nello **Scadenzario** vedrò questa fattura con **Data emissione,** il giorno,mese e anno di quando ho emesso la fattura e come **Data scadenza** le diverse scadenze del pagamento specificato precedentemente.

![](../.gitbook/assets/fatturedivenditaincassiepagamenti.png)

![](../.gitbook/assets/interfacciascandezario.png)

### Chiudere una fattura

Quando la **Fattura di vendita** è stata pagata dal cliente, per non visualizzarla più nello **Scadenzario** si possono adottare **3** metodi differenti:

#### 1. Da emessa a pagato

Quando una **fattura** è stata pagata è possibile toglierla dallo **Scadenzario** cambiando lo stato della fattura da **Emessa** a **Pagato.** Esempio:

![](../.gitbook/assets/stato.png)

#### 2. Da record

Quando una **fattura** è stata pagata o parzialmente pagata è possibile toglierla dallo **Scadenzario** cliccando sopra al record e andando ad inserire in **Pagato** quanto il cliente ha pagato e successivamente cliccare su ![](../.gitbook/assets/salva%20%282%29%20%282%29%20%283%29.png) . Esempio:

![](../.gitbook/assets/metodo2.png)

#### 3. Da record\(più completo\)

Quando una **fattura** è stata pagata è possibile toglierla dallo **Scadenzario** cliccando sopra al record e successivamente cliccando il tasto ![](../.gitbook/assets/aggiungiprimanota.png) , dove apparirà questa schermata:

![](../.gitbook/assets/metodo3.png)

Cliccando su ![](../.gitbook/assets/+aggiungi.PNG) andrò ad aggiungere il movimento in prima nota:

![](../.gitbook/assets/metodo3-1.png)

Così facendo la **fattura** non sarà presente nello **Scadenzario** e sarà visibile il movimento in **Prima nota.**

### Caratteristiche

Al momento nello **Scadenzario** sono presenti sia le **Fatture di acquisto** sia le **Fatture di vendita.** Le fatture con importo **positivo** sono **Fatture di vendita,** le fatture con importo **negativo** sono **Fatture di acquisto.** Nelle prossime versioni è prevista la divisione dello **Scadenzario** in **Scadenzario Fatture di vendita** e **Scadenzario Fatture di acquisto.**

Per tenere traccia dei pagamenti scaduti e da effettuare è necessario filtrare la ricerca andando ad inserire in **Data scadenza** mese e anno, nel seguente formato: mese/anno es. 02/2019. Cosi' facendo vedrò i pagamenti scaduti e da effettuare nel mese e anno selezionato. Il filtraggio può essere fatto anche solo digitando l'anno es: 2018.

{% hint style="warning" %}
I pagamenti scaduti e da effettuare che vanno oltre la **Data di scadenza** saranno visualizzati in **rosso.**
{% endhint %}

![](../.gitbook/assets/pagamentiscadutiodaeffettuare%20%281%29.png)

### Stampa

Il gestionale offre anche delle opzioni di **stampa**,presenti sotto la tabella, quali:

* **Stampa scadenzario:** effettua la stampa di tutti i record presenti nello scadenzario.
* **Scadenzario clienti:** effettua la stampa dei clienti quindi delle **Fatture di vendita**.
* **Scadenzario fornitori**: effettua la stampa dei fornitori quindi delle **Fatture di acquisto.**

![](../.gitbook/assets/stampascadenzario.png)

{% hint style="info" %}
Se si filtra la ricerca nello **Scadenzario** la stampa visualizzerà solo i record filtrati
{% endhint %}

