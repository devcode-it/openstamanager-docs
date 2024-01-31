---
description: Come gestire gli aggiornamenti di OpenSTAManager
---

# 🔝 Aggiornamenti

{% hint style="info" %}
Il modulo **Aggiornamenti** offre diverse possibilità, quali:

* Caricare un aggiornamento
* Controllare il gestionale
* Cercare aggiornamenti
* Verificare i requisiti
{% endhint %}

![](<../../../.gitbook/assets/image (490).png>)

In questo modulo si possono trovare quattro sezioni:

* [Carica un aggiornamento](aggiornamenti.md#carica-un-aggiornamento)
* [Verifica l'integrità dell'installazione](aggiornamenti.md#verifica-lintegrita-dellinstallazione)
* [Ricerca aggiornamenti](aggiornamenti.md#ricerca-aggiornamenti)
* [Requisiti](aggiornamenti.md#requisiti)

### ⬆️ Carica un aggiornamento

Per caricare un aggiornamento si deve cliccare su Sfoglia, selezionare la release in formato ZIP da caricare, e cliccare su Carica.

&#x20;                                                      <img src="../../../.gitbook/assets/image (540).png" alt="" data-size="original">

### ⤵️ Verifica l'integrità dell'installazione

In questa sezione sono disponibili tre opzioni:                                                     &#x20;

![](<../../../.gitbook/assets/image (278).png>)

* Controlla file: Mostra l'elenco dei file che presentano checksum diverso da quello registrato nella versione ufficiale.

![](<../../../.gitbook/assets/image (567).png>)

* Controlla database: Mostra l'elenco dei campi a database che presentano una struttura diversa rispetto a quella prevista nella versione ufficiale del gestionale

![](<../../../.gitbook/assets/image (264).png>)

* Controlla gestionale: Verifica le voci del piano dei conti collegate alle anagrafiche, la corrispondenza tra XML FE e Documenti di vendita, e le colonne duplicate per le viste.

![](<../../../.gitbook/assets/image (337).png>)

### 🔍 Ricerca aggiornamenti

Permette di verificare la presenza di aggiornamenti e in caso siano disponibili, scaricarli.

![](<../../../.gitbook/assets/image (569).png>)



### 👁️‍🗨️ Requisiti

Questa sezione mostra che requisiti per il corretto funzionamento di OpenSTAManager vengono soddisfatti e quali no.

![](<../../../.gitbook/assets/image (143).png>)

### Aggiornare da una versione 2.x a una versione successiva

La procedura di aggiornamentonstallazione è la seguente:

* scaricare l’[ultima versione](https://github.com/devcode-it/openstamanager/releases)
* decomprimere lo zip nella cartella dove si trova OSM 2.x
* accedere alla schermata del software via web
* cliccare su “Aggiorna”.

Questi sono gli step per un corretto aggiornamento a una versione > 2.0 del gestionale. In caso di problemi durante l'aggiornamento è consigliato richiedere un nostro intervento scrivendoci tramite apposito contact form [https://openstamanager.com/contattaci/](https://openstamanager.com/contattaci/) e specificando:

* sistema operativo in uso
* software utilizzato per far funzionare OSM (wamp, xampp, singoli software installati manualmente ecc)
* screenshot dell’eventuale errore
* file setup.log generato in fase di installazione, contenente le operazioni eseguite durante l’installazione.
