# Import listini

{% hint style="info" %}
È possibile importare i listini degli articoli in maniera massiva tramite il caricamento di un file CSV.
{% endhint %}

### Procedura

Accedere dal menù di OpenStaManager al modulo [Import](../../strumenti/import.md) e impostare **Articoli** nel menù a tendina, dopo aver selezionato il modulo sarà visibile un nuovo pulsante nella schermata "Scarica esempio CSV".\
Cliccando su questo pulsante si aprirà un file di esempio di come importare i listini tramite il file CSV.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2FieWODcsyGAXzKNZYQysF%2Ffile.png?alt=media)

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LZJeLg23eVDvrCv74U7-887967055%2Fuploads%2F3FjluxAMT0VUOZdhEqXT%2Ffile.png?alt=media)

A questo punto si può iniziare a creare il file CSV per l'importazione dei listini, utilizzare gli stessi nomi delle colonne per automatizzare l'importazione dei dati.\
Per prima cosa è necessario lasciare vuote o eliminare le colonne dalla cononna B (Barcode) alla N (Note) compresa come in foto. \
In base al tipo di listino degli ulteriori campi andranno lasciati vuoti, possiamo distinguerli in:

**Prezzo di listino fisso (non tiene conto delle quantità)**  \
****_Esempio: Riga 2 (screen)_\
Per importare un listino con il prezzo di listino in base alle quantità è necessario inserire il codice dell'articolo nella colonna A (Codice),  nella colonna O (Anagrafica listino) inserire la ragione sociale del cliente/fornitore, le colonne P (Qta minima) e Q (Qta massima) in questo caso vanno lasciate vuote perchè il prezzo di listino non tiene conto delle quantità. Nelle colonne R (Prezzo listino) e S (Sconto listino) vanno inserite le informazioni sul prezzo e lo sconto corrispondente, infine nell'ultima colonna T (Cliente/Fornitore listino) inserire Fornitore  o Cliente in base all'utilizzo del prezzo, acquisto o vendita.&#x20;

**Prezzo di listino in base alle quantità (tiene conto delle quantità)**  \
****_Esempio: Riga 3(screen)_\
Per importare un listino con il prezzo di listino in base alle quantità è necessario inserire il codice dell'articolo nella colonna A (Codice),  nella colonna O (Anagrafica listino) inserire la ragione sociale del cliente/fornitore, le colonne P (Qta minima) e Q (Qta massima) si riferiscono al prezzo quando la quantità acquistata/venduta è all'interno di quel range. Nelle colonne R (Prezzo listino) e S (Sconto listino) vanno inserite le informazioni sul prezzo e lo sconto corrispondente, infine nell'ultima colonna T (Cliente/Fornitore listino) inserire Fornitore  o Cliente in base all'utilizzo del prezzo, acquisto o vendita.&#x20;

{% hint style="danger" %}
Attenzione!  Lasciare vuota le colonne dalla B (Barcode) alla N (Note) come in foto, queste informazioni se inserite modificano l'articolo già registrato.
{% endhint %}

{% hint style="info" %}
La differenza sostanziale dei due tipi di listini descritti sopra è nel tener conto del prezzo in base alle quantità o meno acquistate/vendute, nell'importazione quindi la differenza è presente nelle colonne **Qta minima** e **Qta massima.**\
****Come nel file d'esempio si possono inserire più righe dello stesso articolo per inserire differenti tipi di prezzi.&#x20;
{% endhint %}

Una volta che il file CSV è pronto per essere caricato seguire le istruzioni del modulo [Import](../../strumenti/import.md) per completare l'importazione.

