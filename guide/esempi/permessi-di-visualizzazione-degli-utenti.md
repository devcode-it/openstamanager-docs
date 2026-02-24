---
description: Come gestire i permessi di visualizzazione dei vari gruppi di utenti
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/I8PynmXUVfCOtwZFC1I6/guide/esempi/permessi-di-visualizzazione-degli-utenti
---

# 🧑‍🔧 Permessi di visualizzazione degli utenti

{% hint style="info" %}
In OpenSTAManager è possibile definire diverse categorie di utenti con permessi specifici dal modulo [Strumenti/Utenti e permessi](../../openstamanager/modules/strumenti/gestione-accessi/utentiepermessi.md).
{% endhint %}

#### Esempio

Volendo abilitare la visualizzazione di tutte le attività ad ogni utente registrato come tecnico (anzichè permettere la sola visualizzazione delle proprie), si dovrà:

{% hint style="warning" %}
Accedere come amministratore.&#x20;
{% endhint %}

Abilitare il modulo Viste da Stato dei servizi, in caso sia disattivato (opzione di default).

&#x20;                                                                 <img src="../../.gitbook/assets/image (781).png" alt="" data-size="original"><br>

Da qui, si dovrà selezionare il modulo Attività e andare alla sezione Filtri. E' qui possibile vedere l'elenco dei filtri attivati e attivabili inseriti di default.

Per permettere ai tecnici di visualizzare tutte le attività si dovrà quindi andare a disabilitare il filtro "Mostra interventi ai tecnici coinvolti".

![](<../../.gitbook/assets/image (305).png>)

{% hint style="info" %}
Mostra interventi ai tecnici coinvolti se abilitato permetterà ai tecnici di visualizzare solo le attività che gli sono state assegnate o a cui sono collegati.

Mostra interventi ai clienti coinvolti se abilitato permetterà ai clienti di visualizzare solo le attività richieste.

Mostra interventi ai tecnici assegnati se abilitato permetterà ai tecnici di visualizzare solo le attività a cui sono stati assegnati.
{% endhint %}

