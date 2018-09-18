---
title: Account Gmail
---

Per configurare correttamente un account email Gmail all'interno di OpenSTAManager è necessario completare nel seguente modo le informazioni dell'elemento del modulo [**Account email**](account.md):
 - *Server SMTP*: `smtp.gmail.com`
 - *Username SMTP*: indirizzo email (example@gmail.com, oppure example@domain.com)
 - *Porta SMTP*: `587`
 - *Sicurezza SMTP*: `TLS`

Se l'account da utilizzare è protetto attraverso il sistema di autenticazione a due fattori, visitare la [sezione relativa](autenticazione-a-due-fattori).
In alternativa, procedere con la guida *Applicazione meno sicure*.

## Applicazione meno sicure

Nel caso **non** sia abilitata l'autenticazione a due fattori, è necessario procedere ad abilitare l'accesso da applicazioni meno sicure attraverso le impostazioni dell'account Google: <https://myaccount.google.com/lesssecureapps>.

E' quindi necessario inserire nel campo *Password SMTP* dell'account del gestionale la password originale dell'account Gmail.

## Autenticazione a due fattori

Se l'autenticazione a due fattori è abilitata, è necessario creare una chiave di accesso Google nella sezione dedicata: <https://myaccount.google.com/apppasswords>.

Una volta visitato il link precedente, comparirà il seguente contenuto.
Sarà necessario selezionare il valore `Altra` del campo *Seleziona app*.

{% include figure path="new.png" alt="Creazione nuova chiave" caption="Screenshot della creazione di una nuova chiave" %}

Verrà quindi reso disponibile un campo per la denominazione della nuova chiave.
Una volta compilato il nome, cliccare sul pulsante **Genera**.

{% include figure path="name.png" alt="Denominazione nuova chiave" caption="Screenshot della denominazione della nuova chiave" %}

Comparirà quindi un messaggio di avvertenza relativo all'utilizzo della nuova chiave, che sarà copiabile dal testo evidenziato in giallo.

{% include figure path="ok.png" alt="Nuova chiave" caption="Screenshot della nuova chiave" %}

E' necessario inserire questa chiave nel campo *Password SMTP* dell'account del gestionale.
