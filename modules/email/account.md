---
title: Account email
---

# Account email

{% hint style="info" %}
Il modulo **Account email** permette all’azienda di gestire tutte le informazioni riguardanti gli account email utilizzati da OpenSTAManager per l'eventuale invio di email con contenuti specifici dei diversi moduli.
{% endhint %}

Questo modulo è complementare a [**Template email**](template.md), che si occupa di gestire le informazioni di base dell'email da inviare.

## Navigazione

Il modulo è raggiungibile attraverso il menu laterale del gestionale, sotto il link **Account email** visibile dall'espansione del menu **Gestione email**.

![Screenshot navigazione account email](https://github.com/devcode-it/openstamanager-docs/tree/5242b6a23c677db2f5451152c8e4c4aded3a99cf/.gitbook/assets/navigazioneaccountemail-1.PNG)

## Caratteristiche

La schermata principale del modulo è strutturata secondo la tabella generale predefinita.

![Screenshot interfaccia Account email](../../.gitbook/assets/scrrenshotaccountemail.PNG)

### Creazione

La creazione di nuovi elementi segue il funzionamento standard del gestionale, necessitando il click sul pulsante apposito all'interno dell'intestazione del modulo.

![Screenshot creazione account email](../../.gitbook/assets/add-account-email.PNG)

Viene quindi data la possibilità di completare le informazioni di base del nuovo account email, quali:

* Nome dell'account
* Nome mostrato nelle email
* Indirizzo email

![Screenshot creazione Account email](../../.gitbook/assets/creazioneaccountemail.PNG)

Il completamento di ulteriori informazioni viene permesso dalla schermata di modifica.

### Modifica

La schermata di modifica permette il completamento di tutte le informazioni che possono essere sfruttate per l'accesso all'account email specificato.

In particolare, vengono resi disponibili i seguenti campi relativi alla gestione di account SMTP:

* Server SMTP
* Username SMTP
* Password SMTP
* Porta SMTP
* Sicurezza SMTP

![Screenshot modifica Account email](../../.gitbook/assets/modificaaccountemail.PNG)

Viene inoltre permessa l'impostazione di un qualsiasi account email come predefinito per la creazione di nuovi template e la segnalazione di eventuali bug.

## Particolarità

{% hint style="info" %}
L'account email predefinito impostato nelle versioni precedenti attraverso le impostazioni viene importato come _Account email da Impostazioni_.
{% endhint %}
