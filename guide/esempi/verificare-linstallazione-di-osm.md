---
description: Come verificare la corretta installazione e configurazione di OpenSTAManager
---

# 🔨 Verificare l'installazione di OSM

### 1️Verificare che i requisiti di OSM siano rispettati

L'installazione del gestionale richiede la presenza di un web server Apache con abilitato il [DBMS MySQL](https://www.mysql.com) e il linguaggio di programmazione [PHP](https://php.net).



| PHP | EOL        |                                                        Supportato                                                       |
| --- | ---------- | :---------------------------------------------------------------------------------------------------------------------: |
| 8.1 | 25/11/2024 |         <img src="https://github.githubassets.com/images/icons/emoji/unicode/274c.png" alt="x" data-size="line">        |
| 8.0 | 26/11/2023 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |
| 7.4 | 28/11/2022 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |
| 7.3 | 06/12/2021 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |
| 7.2 | 30/11/2020 |         <img src="https://github.githubassets.com/images/icons/emoji/unicode/274c.png" alt="x" data-size="line">        |



| MYSQL | EOL        |                                                        Supportato                                                       |
| ----- | ---------- | :---------------------------------------------------------------------------------------------------------------------: |
| 8.0   | 01/04/2026 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |
| 5.7   | 21/10/2023 | <img src="https://github.githubassets.com/images/icons/emoji/unicode/2714.png" alt="heavy_check_mark" data-size="line"> |
| 5.6   | 05/02/2021 |         <img src="https://github.githubassets.com/images/icons/emoji/unicode/274c.png" alt="x" data-size="line">        |

Le versioni di PHP supportate sono dalla 7.3 alla 8.0, mentre quelle di MySQL dalla 5.7 alla 8.0.

{% hint style="warning" %}
Il gestionale non è compatibile con MariaDB.
{% endhint %}

Si può verificare se i requisiti vengono rispettati da Strumenti/Aggiornamenti, nella sezione evidenziata.

<figure><img src="../../.gitbook/assets/immagine (68).png" alt=""><figcaption></figcaption></figure>

### 2️Eseguire i controlli sull'integrità dell'installazione

#### Controllo sui file

Il controllo dei file si può effettuare da Strumenti/Aggiornamenti cliccando su Controlla file.

<figure><img src="../../.gitbook/assets/immagine (51).png" alt=""><figcaption></figcaption></figure>

Qui verranno elencati tutti i file che presentano modifiche rispetto a quelli registrati nella versione ufficiale.

{% hint style="warning" %}
Questa funzionalità potrebbe presentare dei risultati falsamente positivi, sulla base del contenuto del file checksum.json
{% endhint %}

<figure><img src="../../.gitbook/assets/immagine (503).png" alt=""><figcaption></figcaption></figure>

#### Controllo sul database

Il controllo del database può essere effettuato da Strumenti/Aggiornamenti cliccando su Controlla database.

<figure><img src="../../.gitbook/assets/immagine (47).png" alt=""><figcaption></figcaption></figure>

Qui verranno elencate le tabelle del database che presentano una struttura diversa rispetto a quella prevista nella versione ufficiale del gestionale.

{% hint style="warning" %}
Questa funzionalità può presentare dei risultati falsamente positivi, sulla base del contenuto del file database.json o nel caso di aggiornamento del database alla versione 8.0.30 di MySQL.
{% endhint %}

<figure><img src="../../.gitbook/assets/immagine (50).png" alt=""><figcaption></figcaption></figure>

#### Controllo sul gestionale

Il controllo sul gestionale può essere effettuato da Strumenti/Aggiornamenti cliccando su Controlla gestionale, e a seguito su Avvia controlli.

<figure><img src="../../.gitbook/assets/immagine (66).png" alt=""><figcaption></figcaption></figure>

Qui verranno effettuati 3 controlli:

1. Se ogni voce del piano dei conti è correttamente collegato a un'anagrafica
2. Se gli importi degli XML delle fatture elettroniche hanno corrispondenza con gli importi delle fatture di vendita
3. Se sono presenti colonne duplicate per le Viste

<figure><img src="../../.gitbook/assets/immagine (618).png" alt=""><figcaption></figcaption></figure>

### 3️Verificare la presenza di personalizzazioni

Nel caso siano presenti personalizzazioni, esse verranno elencate nella parte superione della pagina in Strumenti/Aggiornamenti.

<figure><img src="../../.gitbook/assets/immagine (177).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Le personalizzazioni possono essere effettuate sul modulo o sul database, e in caso siano presenti l'aggiornamento del gestionale senza il supporto dell'assistenza ufficiale è altamente sconsigliato.
{% endhint %}

Sotto la tabella contenente le personalizzazioni è possibile trovare l'elenco dei moduli modificati:

<figure><img src="../../.gitbook/assets/immagine (616).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Nel caso in cui queste verifiche vengano superate e non si sia riusciti a risalire alla causa del problema, vi invitiamo a contattare l'assistenza.
{% endhint %}

