---
description: Elenco delle principali novità introdotte con la release 2.11
---

# 📣 Novità

Di seguito le principali novità della versione 2.11, per maggiori dettagli visitare [GitHub](https://github.com/devcode-it/openstamanager).

#### **Introdotte azioni di gruppo sui documenti**

E' ora possibile duplicare massivamente i documenti, sono state aggiunte le colonne Data insoluto, Data pagamento rate e Validità nelle fatture di vendita. E' ora possibile creare contratti a partire dagli ordini, importare gli ordini nelle attività e rinnovare contratti con ore residue

#### **Nuove funzionalità commerciali**

E' stata introdotta la gestione delle varianti direttamente a partire dalla scheda articolo, la gestione degli stati impianto con relativo modulo, e l'imputazione di commissioni per riba insolute in fase di registrazione insoluto.

#### **Miglioramenti operativi e di gestione**

E' ora gestita la pausa nelle sessioni, vengono registrate le informazioni relative al Token sessione/Ultimo login nell'utente, è stata aggiunta la selezione della sede destinazione in fase di importazione delle fatture elettroniche, ed è stato aggiunto un modulo Link navbar per aggiungere collegamenti personalizzabili al menu superiore

#### **Sicurezza e integrazioni**

Adeguamento al tracciato SDI 1.9.1, gestione login OAuth2 con Keycloak, firma GDPR con selezione condizioni, stampa GDPR in anagrafica ed estesa compatibilità a php8.5, MySQL8.4 e MariaDB12.2

#### **Ottimizzazioni e refactoring**

Conversione naming tabelle/colonne in snake\_case, allineamento query MariaDB, tour guidato per moduli principali, ottimizzazione importazioni e invio fatture elettroniche con tracking fallite
