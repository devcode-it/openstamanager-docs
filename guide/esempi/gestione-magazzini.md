---
description: Guida alla gestione dei magazzini aggiuntivi in OpenSTAManager
---

# 🗳️ Gestione magazzini

In OpenSTAManager è possibile gestire più magazzini e sedi, dal plugin Sedi all'interno di una determinata anagrafica.

Accedendo al plugin sedi dall'anagrafica della nostra azienda è possibile quindi registrare le sedi collegate e gestire magazzini dove a esempio andare a registrare i beni non destinati alla vendita (cespiti).

Per registrare una nuova sede sarà sufficiente cliccare sul tasto (+).

![](<../../.gitbook/assets/immagine (1011).png>)

Oltre alla sede legale ora saranno disponibili due sedi aggiuntive e un magazzino Cespiti, in cui si andranno a registrare tutti i beni non destinati alla vendita che l'azienda acquisirà.

### Dal modulo movimenti

E' possibile spostare un articolo di magazzino da una sede all'altra dal modulo Magazzino/Movimenti, cliccando sul tasto (+) per creare un nuovo movimento.

![](<../../.gitbook/assets/immagine (728).png>)

Qui si dovranno andare a selezionare la sede di partenza e di destinazione dell'articolo, selezionando come causale "Spostamento". E poi cliccando su Movimenta per procedere a inserire un altro movimento, o su Movimenta e chiudi per tornare all'elenco dei movimenti.

![](<../../.gitbook/assets/immagine (645).png>)

Tra i movimenti sarà ora possibile vedere il movimento appena effettuato, ovvero una diminuzione di 1 unità nella sede legale, e un aumento di 1 unità nella sede Cespiti.

![](<../../.gitbook/assets/immagine (1014).png>)

### Visualizzare le giacenze per sede

Andando in Magazzino/Giacenze sedi e selezionando la sede Cespiti sarà ora possibile vedere tutti gli articoli presenti in questo magazzino.

![](<../../.gitbook/assets/immagine (771).png>)

### Tramite registrazione di un DDT

E' possibile registrare un DDT in entrata dalla nostra sede a una sede secondaria specificando come causale Trasferimento sede.

![](<../../.gitbook/assets/immagine (1044).png>)

Da qui si dovranno ora specificare la sede di partenza e di arrivo della merce, e inserire come righe gli articoli da spostare.

![](<../../.gitbook/assets/immagine (729).png>)

![](<../../.gitbook/assets/immagine (1049).png>)

Una volta effettuato il trasferimento e impostato il DDT come evaso, si dovrà andare a registrare lo stesso DDT con direzione opposta. Sarà possibile registrare questo DDT direttamente da questa schermata cliccando sul tasto Completa trasferimento tra sedi.

![](<../../.gitbook/assets/immagine (1040).png>)

Il gestionale chiederà ora la conferma a procedere con la generazione del documento. Cliccare su Completa per eseguire l'operazione.

&#x20;                                                                <img src="../../.gitbook/assets/immagine (625).png" alt="" data-size="original">



Verrà così generato un DDT in uscita con stato Evaso con gli stessi estremi di quello registrato in entrata.

![](<../../.gitbook/assets/immagine (961).png>)

Andando ad analizzare i movimenti sarà ora possibile vedere lo spostamento dei prodotti dalla sede legale al punto vendita selezionato.

![](<../../.gitbook/assets/immagine (505).png>)

### Visualizzare le giacenze per articolo

Per visualizzare le giacenze di un determinato articolo si deve andare in Magazzino/Articoli e selezionare l'articolo interessato. Da qui sarà possibile tramite il plugin Giacenze verificare la sua disponibilità e presenza nelle diverse sedi.

![](<../../.gitbook/assets/immagine (1042).png>)
