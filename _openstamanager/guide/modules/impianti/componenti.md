---
title: Modulo Gestione componenti
screen:
  - path: add.png
    alt: "Schermata di creazione"
    title: "Schermata di creazione di un nuovo elemento"
  - path: edit.png
    alt: "Schermata di modifica"
    title: "Schermata di modifica di un elemento"
---

Il modulo **Gestione componenti** è dedicato alla gestione dei *modelli dei componenti* di tutti gli **Impianti** gestiti da OpenSTAManager.

{% include figure path="controller.png" alt="Modulo Gestione componenti" caption="Screenshot del modulo **Gestione componenti**" %}

{% include gallery id="screen" caption="Schermate del modulo" %}

## Navigazione

Il modulo è raggiungibile attraverso il menu laterale del gestionale, sotto il link **Gestione componenti** visibile dall'espansione del menu **MyImpianti**.

## Caratteristiche

Le informazioni dei componenti degli impianti vengono salvate in formato *INI*, secondo il se il seguente standard. *{} = facoltativo*

```ini
[Nome del campo]
tipo = tag_HTML
valore = {"Valore di default"}
{opzioni = "Opzione 1", "Opzione 2", "Opzione 3"}

[Nome del campo]
tipo = tag_HTML
valore = {"Valore di default"}
{opzioni = "Opzione 1", "Opzione 2", "Opzione 3"}
```

La dicitura `tag_HTML` indica la possibilità di inserire all'interno del campo il nome di un qualsiasi tag HTML per l'utilizzo durante la modifica.
In particolare, il gestionale supporta la maggior parte dei campi HTML di input (*input*, *select*, *textarea*, *date*, ...); se necessario, è inoltre possibile utilizzare tag normali (*span*, *p*, ...).

### Esempio

Segue un esempio completo del formato precedente, ottenuto dal sistema di base di OpenSTAManager (`files/my_impianti/componente.ini`).

```ini
[Nome]
tipo = span
valore = "Componente di esempio"

[Marca]
tipo = input
valore =

[Tipo]
tipo = select
valore =
opzioni = "Tipo 1", "Tipo 2"

[Data di installazione]
tipo = date
valore =

[Note]
tipo = textarea
valore =
```

## Particolarità

I contenuti del modulo **Gestione componenti** non vengono salvati a livello di database, ma gestiti come allegati non registrati del modulo **Impianti** e quindi salvati fisicamente nella struttura del gestionale.

Una volta che un componente viene aggiunto ad un impianto avviene il salvataggio delle informazioni all'interno del database.
