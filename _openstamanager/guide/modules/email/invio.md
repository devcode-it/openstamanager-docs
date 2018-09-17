---
title: Invio email
screen:
  - path: button-1.png
    alt: "Pulsante singolo"
    title: "Pulsante di invio singolo"
  - path: button-2.png
    alt: "Pulsante multiplo"
    title: "Pulsante di invio multiplo"
  - path: button-3.png
    alt: "Pulsante multiplo con valore predefinito"
    title: "Pulsante di invio multiplo con valore predefinito"
---

La funzione di invio email è una caratteristica integrata in OpenSTAManager, che si basa sulle strutture fornite dai moduli **Account email** e **Template email** per semplificare la gestone delle informazioni relative.

Il sistema è accessibile all'interno di ogni *record* dei moduli che possiedono almeno un template collegato, ed è accessibile attraverso il pulsante dedicato nella sezione in alto a destra della schermata.

{% include gallery id="screen" caption="Pulsanti per l'invio email" %}

## Completamento

Una volta cliccato sul pulsante relativo al template email da inviare, viene mostrata la seguente struttura grafica che si sovrappone agli altri contenuti (*modal*).

{% include figure path="send.png" alt="Schermata di invio email" caption="Screenshot della schermata di invio email" %}

Viene quindi reso possibile modificare alcuni valori predefiniti del template, quali:
 - Oggetto
 - Contenuto
 - Notifica di lettura
 - Stampe da allegare

Viene inoltre fornita la possibilità, oltre ad impostare manualmente i destinatari, di allegare alcuni upload dell'anagrafica Azienda predefinita e dell'elemento di cui si sta effettuando la condivisione.

## Particolarità

Nel caso l'account email legato al template non sia stato completato correttamente, viene mostrato un messaggio di avvertenza relativo.