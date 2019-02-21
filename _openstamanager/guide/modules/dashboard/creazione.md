---
title: Creazione intervento
---

Utilizzando il calendario presente nella **Dashboard** è possibile aggiungere un intervento trascinando il mouse, come nell'esempio che segue:

{% include figure path="CreazioneAttivita.gif" alt="Creazione intervento" caption="Esempio creazione intervento" %}

Creando un intervento come precedentemente indicato si hanno a disposizione una serie di campi da compilare, quali:

- Cliente
- Sede
- Per conto di
- Zona(definita automaticamente in base al *cliente* selezionato,per maggiori informazioni, visitare la documentazione del modulo [**Zone**](../anagrafiche/zone.md))
- Preventivo
- Contratto
- Impianto
- Componenti
- Data e ora richiesta
- Tipo attività
- Stato
- Richiesta
- Inizio attività
- Fine attività
- Tecnici

{% include figure path="AggiungereIntervento.PNG" alt="Creazione intervento" caption="Campi da compliare" %}

## Creazione impianto al volo

Nella schermata di creazione di una nuovo intervento viene permessa la creazione al volo di un *Cliente* relativa al nuovo record. Questa funzionalità viene permessa dal pulsante dedicato a destra del selettore del campo Impianto.

{% include figure path="CreazioneImpianto.PNG" alt="Creazione intervento" caption="Creazione *impianto* al volo" %}

La gestione della creazione viene quindi delegata al modulo **MyImpianti**, permettendo l’inserimento delle informazioni standard documentate nella sezione relativa attraverso un *modal* sovrapposto al resto del contenuto.

{% include figure path="CreazioneImpianto1.PNG" alt="Creazione intervento" caption="Creazione *impianto* al volo" %}

Una volta completata la creazione in questione, l’*impianto* creato verrà automaticamente selezionata.

{% include figure path="RisultatoCreazioneImpianto.PNG" alt="Creazione intervento" caption=" Risultato creazione *impianto* al volo" %}