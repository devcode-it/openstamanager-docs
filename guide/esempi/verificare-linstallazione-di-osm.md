---
description: Come verificare la corretta installazione e configurazione di OpenSTAManager
---

# 🔨 Verificare l'installazione di OSM

## Verificare che i requisiti di OSM siano rispettati

L'installazione del gestionale richiede la presenza di un web server Apache con abilitato il [DBMS MySQL](https://www.mysql.com) e il linguaggio di programmazione [PHP](https://php.net).



| PHP | EOL        |                                                        Supportato                                                       |
| --- | ---------- | :---------------------------------------------------------------------------------------------------------------------: |
| 8.5 | 20/11/2025 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |
| 8.4 | 21/11/2024 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |
| 8.3 | 23/11/2026 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |



| MYSQL | EOL        |                                                        Supportato                                                       |
| ----- | ---------- | :---------------------------------------------------------------------------------------------------------------------: |
| 8.4   | 30/04/2032 |                           <img src="../../.gitbook/assets/image.png" alt="" data-size="line">                           |
| 8.3   | 10/04/2024 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |
| 8.2   | 14/12/2023 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |
| 8.1   | 25/10/2023 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |
| 8.0   | 30/04/2026 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |

Le versioni di PHP supportate sono dalla 8.3 alla 8.5, mentre quelle di MySQL dalla 8.0 alla 8.4.

{% hint style="warning" %}
Stiamo introducendo la compatibilità con MariaDB
{% endhint %}

Si può verificare se i requisiti vengono rispettati da Strumenti/Aggiornamenti, nella sezione evidenziata.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Incongruenze file e database

In questa sezione è possibile identificare incongruenze tra i valori attesi a database e quelli effettivamente presenti nel software, dovuti a personalizzazioni, aggiornamenti interrotti, o query che possono aver dato errore in fase di aggiornamento.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

#### File personalizzati

In questa sezione vengono riportati i file che sono stati modificati rispetto al checksum presente nello zip della release:

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

#### Tabelle non previste

In questa sezione vengono elencate le tabelle non previste nella versione community edition del gestionale, che possono derivare da interventi dell'utente, personalizzazioni o vecchie tabelle che le query di aggiornamento non sono riuscite a rinominare o rimuovere

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

#### Viste personalizzate

In questa sezione vengono indicate le viste personalizzate dal modulo Viste, indicando il valore atteso (in verde) e quello presente nel gestionale (in rosso), la modifica di questi valori può causare la rottura della query relativa alla vista del modulo. Consigliamo di verificare e allineare le viste personalizzate a seguito di ogni aggiornamento.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

#### Moduli personalizzati

In questa sezione vengono indicate le query dei moduli personalizzati dal modulo Viste, sia dove è stata aggiunta una query custom nel campo options2:

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

sia quando la query originale non corrisponde a quella prevista, a causa di un errore di aggiornamento o una modifica utente:

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

#### Campi personalizzati

In questa sezione vengono evidenziati i campi mancanti a database, i campi modificati, le chiavi esterne assenti e quelle modificate

<figure><img src="../../.gitbook/assets/image (894).png" alt=""><figcaption></figcaption></figure>

#### Impostazioni personalizzate

In questa sezione vengono indicate le impostazioni che hanno a database un valore del campo tipo diverso da quello atteso:

<figure><img src="../../.gitbook/assets/image (895).png" alt=""><figcaption></figcaption></figure>

#### Widgets personalizzati

In questa sezione vengono elencati i widgets che hanno a database una query diversa da quella prevista, e potrebbero quindi non essere allineati, ed eventuali widgets personalizzati:

<figure><img src="../../.gitbook/assets/image (896).png" alt=""><figcaption></figcaption></figure>

### Controlli di integrità

E' possibile effettuare i controlli di integrità sul gestionale in questa apposita sezione:

<figure><img src="../../.gitbook/assets/image (897).png" alt=""><figcaption></figcaption></figure>

Si aprirà quindi una modale con tutti i cotrolli del gestionale disponibili:

<figure><img src="../../.gitbook/assets/image (898).png" alt=""><figcaption></figcaption></figure>

#### Piano dei conti collegato alle anagrafiche

Verifica che le anagrafiche del tipo Cliente e Fornitore abbiano il relativo conto del piano dei conti associato, e permette eventualmente di crearlo

L'operazione di correzione:

* Creerà automaticamente i conti mancanti per le anagrafiche Cliente e Fornitore
* Assegnerà i conti appropriati alle anagrafiche interessate

<figure><img src="../../.gitbook/assets/image (900).png" alt=""><figcaption></figcaption></figure>

#### Conti collegati alle anagrafiche non corrispondenti alle ragioni sociali

Verifica che i conti collegati alle anagrafiche abbiano una descrizione che corrisponde a quella della ragione sociale, o se, in caso di anagrafiche rinominate, i due valori non sono allineati.

L'operazione di correzione:

* Creerà nuovi conti per le anagrafiche con conflitti multipli
* Aggiornerà i movimenti contabili collegati
* Eliminerà i conti vuoti non più utilizzati

<figure><img src="../../.gitbook/assets/image (899).png" alt=""><figcaption></figcaption></figure>

#### Anagrafiche con codici R.E.A. non validi

Verifica che il formato inserito nel campo codice R.E.A. dell'anagrafica sia corretto

<figure><img src="../../.gitbook/assets/image (901).png" alt=""><figcaption></figcaption></figure>

#### Corrispondenze XML FE e Documenti di vendita

Verifica che gli importi della fattura e i dati relativi all'anagrafica associata abbiano corrispondenza:

<figure><img src="../../.gitbook/assets/image (902).png" alt=""><figcaption></figcaption></figure>

#### Colonne duplicate per le Viste

Verifica che non ci siano colonne duplicate per le viste, che darebbero quindi errore nella vista del modulo.

La procedura di correzione:

* Eliminerà i record duplicati nelle tabelle zz\_views e zz\_views\_lang
* Manterrà sempre il record più recente (con ID maggiore) ed eliminerà gli altri

<figure><img src="../../.gitbook/assets/image (903).png" alt=""><figcaption></figcaption></figure>

#### Plugin duplicati per i Moduli

Verifica che non ci siano plugin duplicati per i moduli, che darebbero quindi errore alla vista.

La procedura di correzione:

* Eliminerà i record duplicati nelle tabelle zz\_plugins e zz\_plugins\_lang
* Manterrà sempre il record più recente (con ID maggiore) ed eliminerà gli altri

<figure><img src="../../.gitbook/assets/image (904).png" alt=""><figcaption></figcaption></figure>

#### Integrità tabelle multilingua

Verifica che i record delle tabelle abbiano propria corrispondenza nella relativa tabella \_lang

L'operazione di correzione inserirà i record mancanti nelle tabelle \_lang per tutte le lingue disponibili

<figure><img src="../../.gitbook/assets/image (905).png" alt=""><figcaption></figcaption></figure>

#### Integrità file allegati

Verifica che non ci siano file orfani nel sistema o nel database nella tabella zz\_files.

L'operazione di correzione

* RIMOZIONE FILE ORFANI: Rimuoverà definitivamente tutti i file presenti nel filesystem ma non registrati nel database
* RIMOZIONE RECORD ORFANI: Rimuoverà dal database tutti i record che puntano a file fisici inesistenti
* Libererà spazio su disco e pulirà il database da riferimenti non validi

<figure><img src="../../.gitbook/assets/image (906).png" alt=""><figcaption></figcaption></figure>

#### File .htaccess di sistema

Verifica che il file .htaccess non sia stato modificato.
