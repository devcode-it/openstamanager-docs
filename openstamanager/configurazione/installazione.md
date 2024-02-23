---
description: Come installare OpenSTAManager.
---

# 🎯 Installazione

### 🔖 Requisiti

{% hint style="info" %}
Il software permette in automatico di controllare se l'ambiente di utilizzo presenta una configurazione adeguata per il suo corretto funzionamento.
{% endhint %}

In particolare, viene richiesta la presenza di un _web server_ [Apache](https://httpd.apache.org) con il linguaggio di programmazione [PHP](http://php.net) e il [DBMS MySQL](https://www.mysql.com), richiedendo le seguenti versioni minime:

* PHP >= 7.4 <= 8.0
* MySQL >= 5.7

Nel caso la versione PHP non sia compatibile, viene mostrato immediatamente un messaggio informativo a riguardo.

Successivamente, se il controllo precedente viene soddisfatto, il software verrà effettivamente avviato e sarà possibile procedere nella configurazione.

Viene quindi caricata la pagina per il controllo della configurazione del _web server_, di cui vengono controllati vari componenti:

* Moduli Apache
* Estensioni PHP
* Percorsi di servizio per il software

<figure><img src="../../.gitbook/assets/immagine (195).png" alt=""><figcaption></figcaption></figure>

#### Requisiti hardware

Requisiti minimi:

* 1 CPU
* 2GB di ram
* 200MB di spazio per il gestionale

Requisiti consigliati:

* 2 CPU
* 4GB di ram
* 2GB di spazio per il gestionale

## 🎯 Installazione

#### ⛺ Preparazione:

Aggiornare i pacchetti:

```
sudo apt update && sudo apt upgrade
```

Installare Apache:

```
sudo apt install apache2
```

Abilitare il modulo Rewrite di Apache:

```
sudo a2enmod rewrite
```

Riavviare Apache:

```
sudo systemctl restart apache2
```

Installare MySQL Server:

```
sudo apt install mysql-server
```

Installare PHP, insieme a moduli PHP aggiuntivi per Apache e MySQL con il comando:

```
sudo apt install -y php php-cli php-mysql php-common php-zip php-mbstring php-xmlrpc php-curl php-soap php-gd php-xml php-intl php-ldap
```

Installare i seguenti moduli PHP di uso comune. Questi pacchetti aggiungono il supporto PHP per cURL, JavaScript Object Notation (JSON) e Common Gateway Interface (CGI) con il comando:

```
sudo apt install php-curl php-json php-cgi
```

Accedere alla shell MySQL:

```
sudo mysql -u root -p
```

Creare un database e un utente per OpenSTAManager con il comando:

```
CREATE USER 'utente_osm'@'localhost' IDENTIFIED BY 'PASSWORD';
CREATE DATABASE openstamanager;
GRANT ALL PRIVILEGES ON openstamanager.* TO 'utente_osm'@'localhost';
FLUSH PRIVILEGES;
QUIT
```

{% hint style="warning" %}
Sostituire 'PASSWORD' con la password di accesso al database
{% endhint %}

Editare il file php.ini:

```
sudo nano /etc/php/*/apache2/php.ini
```

{% hint style="warning" %}
Sostituire \* con la versione di php in uso
{% endhint %}

Configurare i parametri come segue:

```
display_errors = Off
max_execution_time = 180
max_input_time = 180
max_input_vars = 5000
memory_limit = 512M
post_max_size = 32M
session.gc_maxlifetime = 1440
upload_max_filesize = 32M
zlib.output_compression = On
```

#### 🐱 Da GitHub

Per procedere all'installazione di OpenSTAManager è necessario seguire i seguenti punti:

1. [Scaricare una release ufficiale del progetto](https://github.com/devcode-it/openstamanager/releases).
2. Creare una cartella (ad esempio `openstamanager`) nella root del _web server_ ed estrarvi il contenuto della release scaricata (per maggiori informazioni, [consultare la documentazione tecnica](installazione.md))
3. Creare un database vuoto (tramite [PHPMyAdmin](http://localhost/phpmyadmin/) o riga di comando).
4. Accedere a [http://localhost/openstamanager](http://localhost/openstamanager) dal vostro browser.

Una volta completate le istruzioni per l'installazione del software, è necessario procedere alla sua configurazione per permetterne il funzionamento nell'ambiente di utilizzo.

#### 🖥️ Da Terminale

Nel caso si stia utilizzando la versione direttamente ottenuta dalla repository di GitHub, è necessario eseguire i seguenti comandi da linea di comando per completare le dipendenze PHP (tramite [Composer](https://getcomposer.org)) e gli assets (tramite [Yarn](https://yarnpkg.com)) del progetto.

```
git clone https://github.com/devcode-it/openstamanager.git
cd openstamanager

# Installazione di composer (è consigliato utilizzare i comandi proposti su https://getcomposer.org/download/)
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"

# Può essere saltato ma meglio scaricare dal sito ufficiale di composer
php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

php composer-setup.php
php -r "unlink('composer-setup.php');"

yarn develop-OSM
```

### ✍️ Licenza

La schermata successiva a quella dei requisiti consiste nella gestione della licenza di utilizzo del software.

<figure><img src="../../.gitbook/assets/immagine (577).png" alt=""><figcaption></figcaption></figure>

OpenSTAManager viene reso disponibile tramite la licenza **GPL-3.0**, che ne permette l'uso commerciale e la personalizzazione a patto di mantenere un riferimento al progetto iniziale rimuovendo la responsabilità di eventuali problematiche agli sviluppatori originali.

Una volta accettata la licenza, cliccare su **Successivo**.

{% hint style="warning" %}
**Non è possibile procedere all'utilizzo del software senza aver accettato la licenza.**
{% endhint %}

![Errore di licenza](../../.gitbook/assets/license-error.png)

### ⛵ Database

Una volta corretti i requisiti e accettata la licenza, viene resa disponibile la pagina dedicata alla configurazione del software per l'accesso al database MySQL.

<figure><img src="../../.gitbook/assets/immagine (136).png" alt=""><figcaption></figcaption></figure>

E' possibile, una volta completate le informazioni di configurazione, procedere ad un test automatico per controllare se il database presente è completamente compatibile con il gestionale. Questa funzione è disponibile attraverso il pulsante **Testa il database**.

![Test ok](../../.gitbook/assets/config-ok.png)

In ogni caso, si possono verificare degli errori duranti il salvataggio della configurazione se:

* I dati di connessione sono errati

<figure><img src="../../.gitbook/assets/immagine (544).png" alt=""><figcaption></figcaption></figure>

* I permessi di creazione e scrittura sul file `config.inc.php` sono troppo restrittivi

![Errore di test](../../.gitbook/assets/write-error.png)

Se le credenziali inserite sono corrette, dopo aver cliccato su **Installa** si verrà reindirizzati alla procedura automatica di installazione del database.

#### 🛰️ Installazione del database

Una volta inseriti correttamente i parametri di configurazione, è sufficiente cliccare sul pulsante ![](../../.gitbook/assets/Installa!.PNG) per avviare l'installazione del database di OpenSTAManager.

<figure><img src="../../.gitbook/assets/immagine (553).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/immagine (545).png" alt=""><figcaption></figcaption></figure>

Appena l'installazione sarà terminata, sarà possibile cliccare su Continua e procedere con l'inizializzazione del gestionale.

<figure><img src="../../.gitbook/assets/immagine (552).png" alt=""><figcaption></figcaption></figure>
