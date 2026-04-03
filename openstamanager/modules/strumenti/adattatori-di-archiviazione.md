---
description: Come gestire gli adattatori di archiviazione con OpenSTAManager
icon: folder
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/J2nSTzHfzyz9ea0M9aP3/openstamanager/modules/strumenti/adattatori-di-archiviazione
---

# Adattatori di archiviazione

OpenSTAManager prevede di default il salvataggio dei dati su una cartella files nella root del gestionale. Tramite questo modulo è possibile definire invece un'unità esterna per l'archiviazione dei files.

Di default, come si può vedere dal modulo, è selezionato un Adattatore locale:

<figure><img src="../../../.gitbook/assets/image (841).png" alt=""><figcaption></figcaption></figure>

E' possibile definire una cartella FTP esterna creando un nuovo adattatore cliccando sul tasto +.

Il nuovo adattatore dovrà riportare la configurazione corretta nel campo Options, in formato JSON, così strutturata:

{"host":"HOST","username":"USERNAME","password":"PASSWORD,"root":"PERCORSO"}

al parametro root, andrà inserito il nome della cartella (o il percorso) FTP dove andranno i file caricati dal gestionale.
