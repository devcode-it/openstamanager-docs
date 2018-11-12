---
title: Account Aruba
---

Per configurare correttamente un account email Aruba all'interno di OpenSTAManager è necessario completare nel seguente modo le informazioni dell'elemento del modulo [**Account email**](account.md):
 - *Server SMTP*: `smtp.miodominio.ext`
 - *Username SMTP*: indirizzo email (example@miodominio.ext, oppure example@miodominio.ext)
 - *Porta SMTP*: `25`
 - *Sicurezza SMTP*: `Nessuna`
 
 
 
## Particolarità

Nel caso in cui si continui a verificare l'errore: `PHPMailer: SMTP Error: Could not connect to SMTP host`, provare a disabilitare l'estensione PHP `openssl`.
