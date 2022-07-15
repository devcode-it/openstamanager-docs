---
description: Come gestire i contratti a ore con OpenSTAManager
---

# ⏱ Contratti a ore

Per gestire il **Consuntivo** di un contratto a ore è necessario [creare un Contratto](https://github.com/devcode-it/openstamanager-docs/blob/master/esempi/broken-reference/README.md), e successivamente creare delle **Attività** collegate.

Per poter far ciò, al momento della creazione di un **Contratto**, si deve selezionare uno **Stato dei Contratti** che risulti pianificabile.

![](<../../.gitbook/assets/immagine (6).png>)

Lo stato dei contratti è verificabile in Strumenti/Tabelle/Stati dei contratti.

![](<../../.gitbook/assets/immagine (39).png>)

![](<../../.gitbook/assets/immagine (24).png>)

Si potrà ora [creare un'**Attività**](../../openstamanager/modules/attivita/creazione.md) a cui collegare il **Contratto** appena creato. Le ore di lavoro inserite verranno scalate dal **Budget ore** del contratto.

![](<../../.gitbook/assets/immagine (78).png>)

Per verificarne il **Consuntivo,** si dovrà ora aprire il contratto da Vendite/Contratti e selezionare il Plugin **Consuntivo**.

![](<../../.gitbook/assets/immagine (57).png>)

Da questa schermata è ora possibile verificare la lista delle **Attività** associate a questo contratto, l'ammontare del **Budget ore** disponibile e le ore erogate/residue.
