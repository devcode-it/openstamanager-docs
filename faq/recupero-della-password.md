# Recupero della password

Non esiste una procedura semplificata per permettere il recupero della password degli account di amministrazione \(di default, _admin_\) o di quelli comuni. Si ricorda che è comunque possibile **cambiare** la password in ogni momento, se è stato effettuato l'accesso, attraverso l'utilizzo del modulo **Utenti e permessi** \(**Gestione permessi** per versioni precedenti alla 2.3\) disponibile sotto la dicitura **Strumenti**.

Può però essere necessario **reimpostare** la password, in particolare se è stata dimenticata, per ripristinare l'accesso ad OpenSTAManager.

## Account comune

Per procedere alla reimpostazione della password di un account comune \(non amministrativo\) è necessario accedere con un account amministrativo e utilizzare il modulo **Utenti e permessi** \(**Gestione permessi** per versioni precedenti alla 2.3\), disponibile sotto la dicitura **Strumenti**. In particolare, una volta entrati nella corretta categoria di accesso \(_Agenti_, _Amministratori_, _Clienti_, ...\) dell'account da modificare, è possibile utilizzare la procedura semplificata di cambio password attraverso l'_icona del lucchetto aperto_.

{% hint style="warning" %}
Nel caso non sia possibile accedere con un account amministrativo, contattare l'amministratore.
{% endhint %}

## Account amministrativo

Per reimpostare la password di un account amministrativo è possibile procedere in due modi:

* Se esiste un altro account amministrativo, seguire la procedura precedente per gli account comuni;
* Accedere al database ed eseguire la seguente query:

  ```sql
    UPDATE `zz_users` SET `password` = MD5('nuova_password') WHERE `username` = 'admin';
  ```

