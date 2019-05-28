# Novità 2.4.9

#### Aggiunto \(Added\)

* Possibilità di ricalcolare le scadenze delle **Fatture di acquisto** importate da fatture elettroniche
* Campo _Data registrazione_ e _Data competenza_ per le **Fatture di acquisto**
* Stampa **Preventivo** senza costi totali
* Impostazione di esportazione massiva degli XML delle **Fatture di vendita**
* Impostazioni "Riferimento dei documenti nelle stampe" e "Riferimento dei documenti in Fattura Elettronica" per permettere l'inclusione o meno delle relative diciture in stampe e Fattura Elettronica
* Supporto all'importazione delle Fatture Elettroniche Semplificate e alle notifiche ZIP
* Sistema di confronto dei totali delle Fatture Elettroniche importate \(totale nel file XML\) con il totale calcolato dal gestionale per la visualizzazione grafica di eventuali errori di arrotondamento
* Pulsante per impostare la Fatture Elettroniche remota come processata **\(integrazione con sistemi interni\)**
* Modulo **Stato dei servizi** per la gestione di widget e moduli, e la visualizzazione dello spazione occupato
* Sistema di hook \(e notifiche\) per l'esecuzione automatica di alcune azioni periodiche
  * Controllo automatico della presenza di Fatture Elettroniche da importare **\(integrazione con sistemi interni\)**
  * Controllo automatico della presenza di ricevute di Fatture Elettroniche rilasciate **\(integrazione con sistemi interni\)**
* Possibilità di duplicare gli **Impianti**

#### Modificato \(Changed\)

* La marca da bollo considera solo le righe con esenzione iva da natura N1 a N4, ed è modificabile manualmente a livello di fattura
* Gli sconti incodizionati sono ora gestiti a tutti gli effetti come righe
* Miglioramento della procedura di interpretazione degli XML codificati in P7M \(basata sulla libreria OpenSSL\)
* Aggiornati gli stylesheet per le notifiche della Fattura elettronica
* Possibilità di ricercare per valori maggiori/uguali o minori/uguali sui campi delle tabelle \(importi\)
* Spostamento della gestione di widget e moduli da **Aggiornamenti** al modulo **Stato dei servizi**
* I totali vengono visualizzati e arrotondati sempre a due cifre per legge \(la modifica consiste **solo nella visualizzazione dei totali**, e non influenza i conteggi in alcun modo\)
* Modernizzazione del plugin _Statistiche_ nel modulo **Anagrafiche**

#### Fixed

* Fix selezione righe multiple sulle tabelle
* Fix dei conteggi dei widget _Acquisti_ e _Fatturato_ \(esclusione dell'IVA\)
* Fix dei ripristini delle quantità evase nei **Preventivi** e nei **Contratti**
* Fix API per APP OSM
* Fix per compatibilità con MySQL 8
* Risolti altri bug generali

