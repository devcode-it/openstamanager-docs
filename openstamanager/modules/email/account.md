---
description: Come configurare un account email in OpenSTAManager
icon: circle
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/I8PynmXUVfCOtwZFC1I6/openstamanager/modules/email/account
---

# Account email

{% hint style="info" %}
Il modulo **Account email** permette all’azienda di gestire tutte le informazioni riguardanti gli account email utilizzati da OpenSTAManager per l'eventuale invio di email con contenuti specifici dei diversi moduli.
{% endhint %}

Questo modulo è complementare a [**Template email**](template.md), che si occupa di gestire le informazioni di base dell'email da inviare.

Il modulo si presenta con la seguente schermata:

<figure><img src="../../../.gitbook/assets/immagine (203).png" alt=""><figcaption></figcaption></figure>

## Creazione

Cliccando sul tasto (+) è possibile registrare un nuovo account email.

Viene quindi data la possibilità di completare le informazioni di base del nuovo account email, quali:

* Nome dell'account
* Nome visualizzato nelle email
* Indirizzo email

<figure><img src="../../../.gitbook/assets/immagine (204).png" alt=""><figcaption></figcaption></figure>

## Modifica

La schermata di modifica permette il completamento di tutte le informazioni che possono essere sfruttate per l'accesso all'account email specificato.

In particolare, vengono resi disponibili i seguenti campi relativi alla gestione di account SMTP:

* Server SMTP
* Porta SMTP
* Sicurezza SMTP
* Username SMTP
* Password SMTP

<figure><img src="../../../.gitbook/assets/immagine (205).png" alt=""><figcaption></figcaption></figure>

Viene inoltre permessa l'impostazione di un qualsiasi account email come predefinito per la creazione di nuovi template e la segnalazione di eventuali bug.

{% hint style="info" %}
L'account email predefinito impostato nelle versioni precedenti viene importato come _Account email da Impostazioni_.
{% endhint %}

{% hint style="warning" %}
Per consentire a OpenSTAManager di comunicare in modo sicuro con il servizio email, è necessario [configurare l'OAuth2](../../../configurazioni/configurazione-oauth2.md).
{% endhint %}

## Configurazioni

Come configurare correttamente OpenSTAManager con il servizio di hosting:

### Aruba

Per configurare correttamente un account email Aruba all'interno di OpenSTAManager è necessario inserire le seguenti informazioni:

* **Server SMTP:**
  * per caselle dominio: `smtps.aruba.it`
  * per caselle @aruba.it o @technet.it: `smtp.aruba.it`
* **Porta SMTP**: `465`
* **Non verificare il certificato SSL**: `Disattivato`
* **Sicurezza SMTP**: `SSL`
* **Email mittente**: `email-esempio@aruba.it`
* **Username SMTP**: `Nome-utente-da-visualizzare`
* **Password SMTP**: `password`

<figure><img src="../../../.gitbook/assets/immagine (206).png" alt=""><figcaption></figcaption></figure>

### Gmail

{% hint style="info" %}
Per configurare correttamente un account email Gmail all'interno di OpenSTAManager è necessario inserire le seguenti informazioni nel modulo [Account email](account.md):
{% endhint %}

* _Server SMTP_: `smtp.gmail.com`
* _Username SMTP_: indirizzo email (example@gmail.com, oppure example@domain.com)
* _Porta SMTP_: `587`
* _Sicurezza SMTP_: `TLS`

<figure><img src="../../../.gitbook/assets/immagine (207).png" alt=""><figcaption></figcaption></figure>

L'account appena configurato può avere abilitata l'autenticazione a due fattori:

### Autenticazione a due fattori

Se l'autenticazione a due fattori è abilitata, è necessario creare una chiave di accesso Google nella sezione dedicata: [https://myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords).

Sarà necessario selezionare il valore `Altra` del campo _Seleziona app_.

![](<../../../.gitbook/assets/image (182).png>)

Verrà quindi reso disponibile un campo per la denominazione della nuova chiave. Una volta compilato il nome, cliccare sul pulsante GENERA.

![](<../../../.gitbook/assets/image (639).png>)

Comparirà quindi un messaggio di avvertenza relativo all'utilizzo della nuova chiave, che sarà copiabile dal testo evidenziato in giallo.

![](<../../../.gitbook/assets/image (281).png>)

{% hint style="warning" %}
A partire dal 30 settembre 2024, le app meno sicure, le app di terze parti o i dispositivi che richiedono l'accesso solo con nome utente e password non saranno più supportati per gli account Google Workspace. Per conoscere le date esatte, consulta la pagina degli Aggiornamenti di Google Workspace. Per continuare a utilizzare un'app specifica con il tuo Account Google, dovrai utilizzare un tipo di accesso più sicuro che non condivide i dati delle password. Scopri come utilizzare Accedi con Google.
{% endhint %}

### App meno sicure

{% hint style="danger" %}
DEPRECATA dal 30/05/22: [https://support.google.com/accounts/answer/6010255?hl=it](https://support.google.com/accounts/answer/6010255?hl=it)
{% endhint %}

{% hint style="danger" %}
Per account Gmail che non abbiano abilitato questa impostazione prima che venisse dismessa, è necessario abilitare l'autenticazione a due fattori per la configurazione dell'account nel gestionale.
{% endhint %}

## Invio

{% hint style="info" %}
La funzione di invio email è una caratteristica integrata in OpenSTAManager, che si basa sulle strutture fornite dai moduli **Account email** e **Template email** per semplificare la gestione delle informazioni relative.
{% endhint %}

Il sistema è accessibile all'interno di ogni _record_ dei moduli che possiedono almeno un template collegato, ed è accessibile attraverso il pulsante dedicato nella sezione in alto a destra della schermata.

Una volta cliccato sul pulsante relativo al template email da inviare, apparirà la seguente schermata:

<figure><img src="../../../.gitbook/assets/immagine (208).png" alt=""><figcaption></figcaption></figure>

Viene quindi reso possibile modificare alcuni valori predefiniti del template, quali:

* Oggetto
* Contenuto
* Notifica di lettura
* Stampe da allegare

Viene inoltre fornita la possibilità, oltre di impostare manualmente i destinatari, di allegare alcuni upload dell'anagrafica Azienda predefinita e dell'elemento di cui si sta effettuando la condivisione.
