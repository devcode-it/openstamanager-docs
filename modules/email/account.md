---
title: Account email
description: Come configurare un account email in OpenSTAManager
---

# ✉ Account email

{% hint style="info" %}
Il modulo **Account email** permette all’azienda di gestire tutte le informazioni riguardanti gli account email utilizzati da OpenSTAManager per l'eventuale invio di email con contenuti specifici dei diversi moduli.
{% endhint %}

Questo modulo è complementare a [**Template email**](template.md), che si occupa di gestire le informazioni di base dell'email da inviare.

Il modulo si presenta con la seguente schermata:

![](<../../.gitbook/assets/image (23).png>)

## ➕ Creazione

Cliccando sul tasto (+) è possibile registrare un nuovo account email.

Viene quindi data la possibilità di completare le informazioni di base del nuovo account email, quali:

* Nome dell'account
* Nome visualizzato nelle email
* Indirizzo email

![Screenshot creazione Account email](../../.gitbook/assets/CreazioneAccountEmail.PNG)

## 🖌️ Modifica

La schermata di modifica permette il completamento di tutte le informazioni che possono essere sfruttate per l'accesso all'account email specificato.

In particolare, vengono resi disponibili i seguenti campi relativi alla gestione di account SMTP:

* Server SMTP
* Porta SMTP
* Sicurezza SMTP
* Username SMTP
* Password SMTP

![](<../../.gitbook/assets/image (34).png>)

Viene inoltre permessa l'impostazione di un qualsiasi account email come predefinito per la creazione di nuovi template e la segnalazione di eventuali bug.

{% hint style="info" %}
L'account email predefinito impostato nelle versioni precedenti viene importato come _Account email da Impostazioni_.
{% endhint %}

{% hint style="warning" %}
Per consentire a OpenSTAManager di comunicare in modo sicuro con il servizio email, è necessario [configurare l'OAuth2](../../faq/configurazione-oauth2.md).
{% endhint %}

## 💡 Configurazioni

Come configurare correttamente OpenSTAManager con il servizio di hosting:

### 📘 Aruba

{% hint style="info" %}
Per configurare correttamente un account email Aruba all'interno di OpenSTAManager è necessario inserire le seguenti informazioni nel modulo [Account email](account.md):
{% endhint %}

* _Server SMTP_: `smtp.miodominio.ext`
* _Username SMTP_: indirizzo email (example@miodominio.ext, oppure example@miodominio.ext)
* _Porta SMTP_: `25`
* _Sicurezza SMTP_: `Nessuna`

![](<../../.gitbook/assets/image (52).png>)

{% hint style="warning" %}
Nel caso in cui si continui a verificare l'errore: `PHPMailer: SMTP Error: Could not connect to SMTP host`, provare a disabilitare l'estensione PHP `openssl`.
{% endhint %}

### 📗 Gmail

{% hint style="info" %}
Per configurare correttamente un account email Gmail all'interno di OpenSTAManager è necessario inserire le seguenti informazioni nel modulo [Account email](account.md):
{% endhint %}

* _Server SMTP_: `smtp.gmail.com`
* _Username SMTP_: indirizzo email (example@gmail.com, oppure example@domain.com)
* _Porta SMTP_: `587`
* _Sicurezza SMTP_: `TLS`

![](<../../.gitbook/assets/image (94).png>)

L'account può avere abilitata l'autenticazione a due fattori:

### Autenticazione a due fattori



### Applicazioni meno sicure

####

## 📨Invio

