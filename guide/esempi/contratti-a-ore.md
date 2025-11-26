---
description: Come gestire i contratti a ore con OpenSTAManager
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/LFXMzl7lx1tPtA15nWw7/guide/esempi/contratti-a-ore
---

# ⏱️ Contratti a ore

Per gestire il **Consuntivo** di un contratto a ore è necessario [creare un Contratto](https://github.com/devcode-it/openstamanager-docs/blob/master/esempi/broken-reference/README.md), e successivamente creare delle **Attività** collegate.

Per poter far ciò, il **Contratto** interessato deve essere impostato in uno stato pianificabile (di default: In lavorazione, Fatturato, Pagato e Parzialmente fatturato).

![](<../../.gitbook/assets/immagine (569).png>)

Lo stato dei contratti è verificabile in Strumenti/Tabelle/Stati dei contratti.

![](<../../.gitbook/assets/immagine (605).png>)

![](<../../.gitbook/assets/immagine (851).png>)

Si potrà ora [creare un'**Attività**](../../openstamanager/modules/attivita/creazione.md) a cui collegare il **Contratto** appena creato. Le ore di lavoro inserite verranno scalate dal **Budget ore** del contratto.

![](<../../.gitbook/assets/immagine (971).png>)

Per verificarne il **Consuntivo,** si dovrà ora aprire il contratto da Vendite/Contratti e selezionare il Plugin **Consuntivo**.

![](<../../.gitbook/assets/immagine (619).png>)

Da questa schermata è ora possibile verificare la lista delle **Attività** associate a questo contratto, l'ammontare del **Budget ore** disponibile e le ore erogate/residue.
