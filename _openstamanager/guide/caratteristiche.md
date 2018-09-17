---
title: Caratteristiche
---

OpenSTAManager presenta un'interfaccia generale piuttosto chiara, basata su strutture comuni e solitamente di semplice utilizzo.

## Navigazione

{% include figure path="menu.png" alt="Menu di navigazione" caption="Screenshot del menu di navigazione" class="align-right" %}

La navigazione attraverso le diverse sezioni del gestionale viene resa possibile dal menu laterale, visibile in ogni pagina e rappresentante i moduli a cui l'utente autenticato ha accesso.

Questo menu si compone generalmente di macro-sezioni per argomento (quali **Attività**, **Vendite**, **Acquisti**) che raggruppano diversi moduli al loro interno, generalmente visualizzabili cliccando sulla simbolo <i class="fas fa-chevron-left"></i>.

Il modulo corrente viene evidenziato, nel tema predefinito, con una scritta bianca più vivace delle altre. Per maggiori informazioni sui moduli, visitare la [sezione apposita](#modulo).

Nella parte più alta di questa componente è inoltre presente una barra di ricerca generalizzata all'interno del gestionale, che permette di effettuare ricerche tra i moduli che supportano questa funzione.

## Selezione temporale

Nella sezione in alto a sinistra di ogni modulo è possibile selezionare il periodo temporale a cui il gestionale farà riferimento per l'individuazione delle informazioni di ogni modulo.

Sono presenti diversi valori pre-impostati:
 - Oggi
 - I trimestre
 - II trimestre
 - III trimestre
 - IV trimestre
 - I semestre
 - II semestre
 - Questo mese
 - Mese scorso
 - Quest'anno (*default*)
 - Anno scorso

Questa funzionalità è sfruttata in particolare da moduli in cui il periodo di tempo è rilevante (quali, per esempio, **Attività** e **Fatture**) mentre in altri non provoca alcun effetto (per esempio, **Dashboard** e **Articoli**).

{% include figure path="time.png" alt="Selezione temporale" caption="Screenshot del sistema di selezione temporale" %}

## Opzioni di controllo

Parallelamente alla possibilità di selezionare il periodo temporale, vengono rese disponibili alcune opzioni aggiuntive nella sezione in alto a destra del software.

{% include figure path="options.png" alt="Opzioni" caption="Screenshot delle opzioni generali" %}

Viene qui permesso di procedere alle seguenti azioni, in ordine:
 - Stampare la schermata attuale attraverso il browser
 - Visitare la pagina per la segnalazione dei bug
 - Visitare l'elenco dei propri tentativi di accesso
 - Visitare la pagina di informazioni integrata in OpenSTAManager
 - Effettuare il logout

## Modulo

I moduli sono la componente principale della struttura di OpenSTAManager.
Sono progettati per avere una struttura facilmente personalizzabile e mantenere comportamenti indipendenti dal resto del software.

Ogni modulo si occupa in genere di un singolo argomento, che può essere rappresentato e considerato in vari modi.
La navigazione è permessa attraverso il [menu laterale](#navigazione).

{% include figure path="controller.png" alt="Schermata generale dei moduli" caption="Screenshot della schermata generale di **Anagrafiche**" %}

Ogni modulo gestisce le proprie informazioni in modo indipendente da OpenSTAManager, quindi non è possibile prevedere in modo completo il suo comportamento per l'utente finale.
Per ottenere maggiori informazioni, è necessario visitare la guida relativa al singolo modulo.

### Tabella generale

I moduli più comuni del gestionale presentano, come schermata principale, una tabella in cui è possibile scorrere tutti gli elementi presenti al suo interno.

Cliccando sulla riga dell'elemento interessato, si verrà reindirizzati alla [schermata di modifica del *record*](#modifica-record).

Esempi di questo comportamento sono individuabili in **Anagrafiche**, **Attività**, **Articoli**, e in molti altri moduli predefiniti.

{% include figure path="table.png" alt="Tabella generale dei moduli" caption="Screenshot della tabella generale di **Anagrafiche**" %}

### Contenuti personalizzati

Eventualmente, esistono alcuni moduli con requisiti particolari per la propria schermata principale.
In questi casi, è impossibile prevedere il tipo di informazioni presentabili e la modalità, che dipende dal singolo modulo.

Esempi di questa struttura sono presenti nei moduli **Dashboard** e **Statistiche**.

### Creazione record

I moduli che permettono la creazione di nuovi elementi presentano un pulsante apposito vicino all'intestazione della pagina.
{% include figure path="add-button.png" alt="Pulsante di creazione di un nuovo *record*" caption="Screenshot del pulsante di creazione di un nuovo *record* in **Anagrafiche**" %}

Una volta cliccato il pulsante in questione, verrà aperta una schermata sovrapposta al resto del software per permettere di inserire le informazioni del nuovo elemento.
{% include figure path="add.png" alt="Schermata di creazione di un nuovo *record*" caption="Screenshot della schermata di creazione di un nuovo *record* in **Anagrafiche**" %}

### Modifica record

I moduli che permetto la modifica dei propri elementi visualizzano una schermata apposita dedicata alla gestione delle informazioni complete dei *record*.

Di seguito è possibile osservare una generica schermata che permette la suddetta modifica:
{% include figure path="editor.png" alt="Schermata di modifica del *record*" caption="Screenshot della schermata di modifica del *record* di **Anagrafiche**" %}

## Widget

Ogni modulo può presentare delle strutture denominate *widget*, che si presentano secondo una grafica comune ma possono eseguire una singola azione a seguito del click al di sopra di esse.
In generale, queste componenti sono presenti nella parte alta o bassa della pagina (in base alla configurazione).

E' inoltre possibile che vi sia una differenza tra i widget all'interno della schermata principale del modulo e nella sezione di modifica del *record*.

{% include figure path="widgets.png" alt="Sezione dei widgets" caption="Screenshot della sezione dei widgets in **Anagrafiche**" %}

## Plugin

Ogni modulo può possedere delle sezioni note come *plugin*, che possono essere considerati come dei sotto-moduli per il modulo stesso.
Questi sono navigabili attraverso l'apposito menu a destra dell'intestazione della pagina.

{% include figure path="plugins.png" alt="Sezione dei plugin" caption="Screenshot della sezione dei plugin in **Anagrafiche**" %}

I plugin possono presentare comportamenti molto diversi, e sono in generale separati dal modulo a cui appartengono, malgrado vi siano collegati fortemente.

Per maggiori informazioni, visitare la documentazione dei moduli.

Per gli amministratori, è inoltre presente un plugin *sperimentale* denominato **Info** che permette di visualizzare la cronologia di modifica del *record*.
{: .notice--warning}

## Upload

OpenSTAManager presenta inoltre una struttura comune per la gestione di eventuali upload da parte dell'utente per il singolo elemento del modulo.

Questa funzione, qualora abilitata per il modulo in utilizzo, si presenta nel seguente modo:
{% include figure path="uploads.png" alt="Sezione di gestione degli upload" caption="Screenshot della sezione di gestione degli upload" %}
