---
description: Come gestire le quantità di magazzino in OpenSTAManager
---

# 🏢 Quantità di magazzino

Nel caso magazzino ci presentino articoli con quantità negativa, è possibile procedere ad allinearli cliccando nel rispettivo record.

Dalla schermata di dettaglio dell'articolo, è quindi possibile andare alla sezione Giacenza totale, abilitare Modifica quantità, modificare la quantità desiderata e inserire una Descrizione movimento.

![](<../../.gitbook/assets/image (107).png>)

La quantità dell'articolo ora sarà quella appena selezionata.

Nel modulo **Movimenti** sarà possibile visualizzare il movimento generatosi dall'operazione appena eseguita.

![](<../../.gitbook/assets/image (60).png>)

In alternativa è possibile aggiungere un movimento per allineare la quantità dell'articolo[ dal modulo movimenti.](https://docs.openstamanager.com/modules/magazzino/movimenti#creazione)

## 🤿 Articolo fittizio

{% hint style="info" %}
Nel caso in cui si debba aggiungere un servizio, come ad esempio le spese di spedizione, è possibile farlo creando un nuovo **Articolo.**
{% endhint %}

Il procedimento è uguale a quello di[ Creazione di un Articolo](https://docs.openstamanager.com/modules/magazzino/articoli-1#creazione) ma bisognerà abilitare l'opzione Questo articolo è un servizio, dalla sezione Vendita. Si dovrà inoltre specificare un prezzo di vendita.

![](<../../.gitbook/assets/image (89).png>)

Spuntando la casella **Questo articolo è un servizio** le quantità non saranno considerate, in questo modo rimarranno fisse a **0** mentre il **Prezzo di vendita** sarà il prezzo stabilito per il servizio.

Grazie alla possibilità di aggiungere un articolo fittizio si potranno ad esempio aggiungere le spese di spedizione in un DDT in uscita.
