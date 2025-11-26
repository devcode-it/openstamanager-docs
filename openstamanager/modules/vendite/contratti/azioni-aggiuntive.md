---
description: Guida alle azioni aggiuntive del modulo Contratti di OpenSTAManager
icon: circle-question
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/LFXMzl7lx1tPtA15nWw7/openstamanager/modules/vendite/contratti/azioni-aggiuntive
---

# Azioni aggiuntive

## ● Dal modulo Contratti

Il modulo contratti permette di cambiare stato, cambiare metodo di pagamento, fatturare e rinnovare massivamente i contratti dalle azioni di gruppo.

### ● Fattura contratti

Una volta selezionati i record interessati è possibile fatturare massivamente i contratti cliccando su Azioni di gruppo/Fattura contratti.

{% hint style="warning" %}
Lo stato del contratto deve essere: Accettato, In lavorazione, Concluso o Parzialmente fatturato.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/immagine (82).png" alt=""><figcaption></figcaption></figure>

Il gestionale chiederà quindi la conferma a procedere alla fatturazione, permettendo di scegliere:

* Se aggiungere le righe dei contratti selezionati a una fattura di vendita in bozze dello stesso cliente
* il sezionale in cui andare a registrare la fattura di vendita
* il tipo di documento che si andrà a creare

Cliccando su procedi si confermerà la fatturazione.

<figure><img src="../../../../.gitbook/assets/immagine (83).png" alt=""><figcaption></figcaption></figure>

Sarà ora possibile visualizzare la fattura di vendita appena creata nel modulo Vendite/Fatture di vendita.

![](<../../../../.gitbook/assets/image (101).png>)

![](<../../../../.gitbook/assets/image (585).png>)

### ● Rinnova contratti

Una volta selezionati i contratti interessati è possibile rinnovarli massivamente cliccando su Azioni di gruppo/Rinnova contratti.

<figure><img src="../../../../.gitbook/assets/immagine (85).png" alt=""><figcaption></figcaption></figure>

Il gestionale chiederà quindi la conferma a procedere al rinnovo.

{% hint style="info" %}
Nel contratto devono essere specificate le date di accettazione e conclusione, deve essere impostato come Rinnovabile, e deve trovarsi in uno stato Completato.&#x20;
{% endhint %}

<figure><img src="../../../../.gitbook/assets/immagine (84).png" alt=""><figcaption></figcaption></figure>

Cliccando su Procedi i contratti selezionati verranno rinnovati.

#### Cambia stato <a href="#rinnova-contratti" id="rinnova-contratti"></a>

Con questa azione di gruppo è possibile selezionare uno stato e impostarlo massivamente a tutti i contratti selezionati:

<figure><img src="../../../../.gitbook/assets/immagine (86).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/immagine (88).png" alt=""><figcaption></figcaption></figure>

#### Cambia metodo di pagamento <a href="#rinnova-contratti" id="rinnova-contratti"></a>

Selezionando un metodo di pagamento è possibile applicarlo a  tutti i contratti selezionati:

<figure><img src="../../../../.gitbook/assets/immagine (87).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/immagine (89).png" alt=""><figcaption></figcaption></figure>

## ● Dal dettaglio Contratti

Cliccando su uno specifico record è possibile entrare nella schermata di dettaglio.

Da qui, nella sezione superiore della pagina, è possibile trovare le funzioni:

* Stampa contratto
* Invia
* Crea fattura
* Rinnova...
* Duplica contratto

### ● Stampa contratto

Dalla schermata di dettaglio di un contratto è possibile procedere a diversi tipi di stampe:

* Contratto
* Consuntivo contratto interno
* Consuntivo contratto
* Contratto (senza prezzi)
* Consuntivo contratto (senza prezzi)

![](<../../../../.gitbook/assets/image (432).png>)

Cliccando sul tipo di stampa scelto sarà possibile visualizzare la stampa del documento

![](<../../../../.gitbook/assets/image (275).png>)

### ● Invia

Dalla schermata di dettaglio di un'attività è possibile procedere a inviare via mail:

* Contratto
* Consuntivo contratto

![](<../../../../.gitbook/assets/image (513).png>)

Cliccando sul tipo di documento da inviare si verrà indirizzati al template email compilato con i dati dell'attività, dove sarà possibile inviare la mail cliccando su Invia.

![](<../../../../.gitbook/assets/image (106).png>)

### ● Crea fattura

Dalla schermata di dettaglio di un contratto è possibile procedere alla sua fatturazione cliccando sul tasto Crea fattura.

{% hint style="warning" %}
Il contratto deve avere almeno una riga inserita e il suo stato deve essere: Accettato, In lavorazione, Concluso o Parzialmente fatturato.
{% endhint %}

![](<../../../../.gitbook/assets/image (154).png>)

Si aprirà ora la seguente schermata, in cui sarà possibile selezionare le righe da importare del contratto e impostare le opzioni generali delle righe:

* Rivalsa
* Ritenuta d'acconto
* Se calcolare ritenuta d'acconto sull'imponibile o imponibile + rivalsa
* Il conto da utilizzare

Una volta apportate le necessarie modifiche si dovrà cliccare su Aggiungi per procedere alla creazione della fattura di vendita.

<figure><img src="../../../../.gitbook/assets/immagine (90).png" alt=""><figcaption></figcaption></figure>

Sarà ora possibile visualizzare la fattura di vendita appena creata nel modulo Vendite/Fatture di vendita.

![](<../../../../.gitbook/assets/image (500).png>)

![](<../../../../.gitbook/assets/image (107).png>)

### ● Rinnova

{% hint style="warning" %}
La funzione **Rinnova** viene resa disponibile al verificarsi delle seguenti condizioni:

* E' stata [abilitata](plugin/rinnovi.md) l'opzione _Rinnovabile_ del contratto
* Le date di accettazione e conclusione sono state specificate
* Il contratto si trova in uno stato Completato.
{% endhint %}

![](<../../../../.gitbook/assets/image (236).png>)

Il gestionale chiederà quindi la conferma di procedere al rinnovo del contratto, da confermare cliccando su Rinnova.

<figure><img src="../../../../.gitbook/assets/immagine (91).png" alt=""><figcaption></figcaption></figure>

Sarà ora possibile visualizzare il contratto appena rinnovato nel modulo Contratti.

Esso presenterà le spese e righe del contratto originale, fissando le relative pianificazioni.

![](<../../../../.gitbook/assets/image (564).png>)

### ● Duplica contratto

Dalla schermata di dettaglio di un contratto è possibile procedere alla sua duplicazione cliccando su duplica contratto.

![](<../../../../.gitbook/assets/image (98).png>)

Verrà quindi creata una copia del contratto che presenterà gli stessi dati:

![](<../../../../.gitbook/assets/image (437).png>)
