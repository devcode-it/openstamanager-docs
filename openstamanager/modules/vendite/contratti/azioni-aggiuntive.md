---
description: Guida alle azioni aggiuntive del modulo Contratti di OpenSTAManager
---

# ❗ Azioni aggiuntive

## 👥 Dal modulo Contratti

Il modulo contratti permette di fatturare e rinnovare massivamente i contratti dalle azioni di gruppo.

### 📃 Fattura contratti

Una volta selezionati i record interessati è possibile fatturare massivamente i contratti cliccando su Azioni di gruppo/Fattura contratti.

{% hint style="warning" %}
Lo stato del contratto deve essere: Accettato, In lavorazione, Concluso o Parzialmente fatturato.
{% endhint %}

![](<../../../../.gitbook/assets/image (188).png>)

Il gestionale chiederà quindi la conferma a procedere alla fatturazione, permettendo di scegliere:

* Se aggiungere le righe dei contratti selezionati a una fattura di vendita in bozze dello stesso cliente
* il sezionale in cui andare a registrare la fattura di vendita
* il tipo di documento che si andrà a creare

Cliccando su procedi si confermerà la fatturazione.

![](<../../../../.gitbook/assets/image (202).png>)

Sarà ora possibile visualizzare la fattura di vendita appena creata nel modulo Vendite/Fatture di vendita.

![](<../../../../.gitbook/assets/image (194).png>)

![](<../../../../.gitbook/assets/image (460).png>)

### ⏱️ Rinnova contratti

Una volta selezionati i contratti interessati è possibile rinnovarli massivamente cliccando su Azioni di gruppo/Rinnova contratti.

![](<../../../../.gitbook/assets/image (367).png>)

Il gestionale chiederà quindi la conferma a procedere al rinnovo.

{% hint style="info" %}
Nel contratto devono essere specificate le date di accettazione e conclusione, deve essere impostato come Rinnovabile, e deve trovarsi in uno stato Completato.&#x20;
{% endhint %}

&#x20;                                                    ![](<../../../../.gitbook/assets/image (516).png>)

Cliccando su Procedi i contratti selezionati verranno rinnovati.

## 👤 Dal dettaglio Contratti

Cliccando su uno specifico record è possibile entrare nella schermata di dettaglio.

Da qui, nella sezione superiore della pagina, è possibile trovare le funzioni:

* Stampa contratto
* Invia
* Crea fattura
* Rinnova...
* Duplica contratto

### 🖨️ Stampa contratto

Dalla schermata di dettaglio di un contratto è possibile procedere a diversi tipi di stampe:

* Contratto
* Consuntivo contratto interno
* Consuntivo contratto
* Contratto (senza prezzi)
* Consuntivo contratto (senza prezzi)

![](<../../../../.gitbook/assets/image (170).png>)

Cliccando sul tipo di stampa scelto sarà possibile visualizzare la stampa del documento

![](<../../../../.gitbook/assets/image (176).png>)

### 📧 Invia

Dalla schermata di dettaglio di un'attività è possibile procedere a inviare via mail:

* Contratto
* Consuntivo contratto

![](<../../../../.gitbook/assets/image (163).png>)

Cliccando sul tipo di documento da inviare si verrà indirizzati al template email compilato con i dati dell'attività, dove sarà possibile inviare la mail cliccando su Invia.

![](<../../../../.gitbook/assets/image (156).png>)

### 📃 Crea fattura

Dalla schermata di dettaglio di un contratto è possibile procedere alla sua fatturazione cliccando sul tasto Crea fattura.

{% hint style="warning" %}
Il contratto deve avere almeno una riga inserita e il suo stato deve essere: Accettato, In lavorazione, Concluso o Parzialmente fatturato.
{% endhint %}

![](<../../../../.gitbook/assets/image (39).png>)

Si aprirà ora la seguente schermata, in cui sarà possibile selezionare le righe da importare del contratto e impostare le opzioni generali delle righe:

* Rivalsa
* Ritenuta d'acconto
* Se calcolare ritenuta d'acconto sull'imponibile o imponibile + rivalsa
* Il conto da utilizzare

Una volta apportate le necessarie modifiche si dovrà cliccare su Aggiungi per procedere alla creazione della fattura di vendita.

![](<../../../../.gitbook/assets/image (212).png>)

Sarà ora possibile visualizzare la fattura di vendita appena creata nel modulo Vendite/Fatture di vendita.

![](<../../../../.gitbook/assets/image (139).png>)

![](<../../../../.gitbook/assets/image (162).png>)

### 🔄 Rinnova

{% hint style="warning" %}
La funzione **Rinnova** viene resa disponibile al verificarsi delle seguenti condizioni:

* E' stata [abilitata](plugin/rinnovi.md) l'opzione _Rinnovabile_ del contratto
* Le date di accettazione e conclusione sono state specificate
* Il contratto si trova in uno stato Completato.
{% endhint %}

![](<../../../../.gitbook/assets/image (207).png>)

Il gestionale chiederà quindi la conferma di procedere al rinnovo del contratto, da confermare cliccando su Rinnova.

![](<../../../../.gitbook/assets/image (182).png>)

Sarà ora possibile visualizzare il contratto appena rinnovato nel modulo Contratti.

Esso presenterà le spese e righe del contratto originale, fissando le relative pianificazioni.

![](<../../../../.gitbook/assets/image (209).png>)

### 🧬 Duplica contratto

Dalla schermata di dettaglio di un contratto è possibile procedere alla sua duplicazione cliccando su duplica contratto.

![](<../../../../.gitbook/assets/image (203).png>)

Verrà quindi creata una copia del contratto che presenterà gli stessi dati:

![](<../../../../.gitbook/assets/image (190).png>)
