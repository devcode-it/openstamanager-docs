---
title: Account Aruba
---

# Aruba

{% hint style="info" %}
Per configurare correttamente un account email Aruba all'interno di OpenSTAManager è necessario completare nel seguente modo le informazioni dell'elemento del modulo [**Account email**](account.md):
{% endhint %}

* _Server SMTP_: `smtp.miodominio.ext`
* _Username SMTP_: indirizzo email (example@miodominio.ext, oppure example@miodominio.ext)
* _Porta SMTP_: `25`
* _Sicurezza SMTP_: `Nessuna`

![Screenshot creazione account email aruba](<../../.gitbook/assets/accountemail (1) (1) (2) (1) (1).PNG>)

## Particolarità

{% hint style="warning" %}
Nel caso in cui si continui a verificare l'errore: `PHPMailer: SMTP Error: Could not connect to SMTP host`, provare a disabilitare l'estensione PHP `openssl`.
{% endhint %}
