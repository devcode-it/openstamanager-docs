---
description: Come effettuare un backup dei dati in OpenSTAManager
---

# ⏸ Backup

OpenSTAManager include un sistema integrato di backup, che permette di salvare le informazioni dell'installazione in un percorso predefinito secondo la configurazione indicata.

## 📗 Configurazione

Il backup presenta alcune impostazioni configurabili dall'utilizzatore in relazione alle operazioni di [backup automatico](backup.md#backup-automatico) e al percorso di salvataggio dei backup stessi.

Il percorso di backup può essere configurato nel file `config.inc.php`:

```
// Percorso della cartella di backup
$backup_dir = __DIR__.'/backup/';
```

{% hint style="warning" %}
Per motivi di sicurezza si consiglia di modificare il percorso della cartella di backup al di fuori della cartella di OSM, possibilmente in una unità esterna.
{% endhint %}

### 📗 Modulo

Esiste un modulo apposito, **Backup**, che permette di visualizzare in ogni momento le informazioni relative alla configurazione dei backup e di gestire i backup presenti del gestionale.

Per creare un nuovo backup si dovrà cliccare su Crea backup.

![](<../../.gitbook/assets/immagine (68) (1).png>)

### 📗 Formato dei backup

Il backup di OpenSTAManager viene gestito secondo due procedure diverse sulla base della configurazione PHP del server: se è installata [l'estensione ZIP](https://www.php.net/manual/en/book.zip.php) viene generato un singolo archivio `.zip`, altrimenti viene creata una cartella apposita per il backup.

In entrambi i casi, i backup presentano la stessa struttura interna poiché contengono tutti i file del gestionale con l'unica aggiunta di un file `database.sql` nel percorso principale, che contiene l'intero database in cui il gestionale è installato risalente al momento di esecuzione del backup.

{% hint style="warning" %}
Per migliorare la sicurezza del server, il file `config.inc.php`, che contiene i dati di accesso al database, non viene mai incluso nel backup.
{% endhint %}

## 📘 Ripristino

Esiste una procedura semplificata di ripristino dei backup, che cerca di risolvere il problema tecnico per utenti con meno esperienza tecnica. Si dovrà cliccare Ripristina nel backup interessato, dalla sezione Backup compressi.

![](<../../.gitbook/assets/immagine (50) (1) (1).png>)

La procedura manuale è comunque sempre disponibile, e prevede di:

* Creare una cartella vuoto dove estrarre/copiare il contenuto del backup
* Creare un nuovo database, per poi importare il file `database.sql` dalla cartella del ripristino
* Rimuovere il file `database.sql` dalla cartella del ripristino
* Procedere alla configurazione del database per il gestionale (tramite procedura semplificata o impostazione manuale del file `config.inc.php`)

![](<../../.gitbook/assets/immagine (41) (1) (1).png>)

## 📙 Backup automatico

E' disponibile una impostazione nativa per l'esecuzione del backup al primo accesso giornaliero: nel modulo **Impostazioni**, sotto la categoria **Backup** è sufficiente selezionare _Backup automatico_.

![Opzioni disponibili per i backup](<../../.gitbook/assets/image (5).png>)

Il backup automatico viene eseguito in modi diversi a seconda della versione del gestionale installata:

* per versioni < 2.4.11 il backup viene eseguito durante la procedura di login del primo utente;
* dalla versione 2.4.11 in poi, è presente un _hook_ indipendente che effettua il backup in background.
