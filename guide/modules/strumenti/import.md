---
title: Import
---

# Import

{% hint style="info" %}
Il modulo **Import** permette di caricare dei file CSV per aggiungere dei record nel modulo _Articoli_ o _Anagrafiche._
{% endhint %}

![Screenshot interfaccia import](../../../.gitbook/assets/screenimport.PNG)

## Navigazione

Il modulo è raggiungibile attraverso il menu laterale del gestionale, sotto il link **Strumenti**.

![Screenshot interfaccia navigazione](../../../.gitbook/assets/navigazioneimport.PNG)

## Creazione

La creazione di nuovi elementi segue il funzionamento standard del gestionale, necessitando il click sul pulsante apposito all'interno dell'intestazione del modulo.

![Screenshot creazione import](../../../.gitbook/assets/aggiuntaimport.PNG)

![Screenshot creazione import](../../../.gitbook/assets/aggiungiimport.PNG)

Proseguendo con il click sul tasto ![](../../../.gitbook/assets/+aggiungi%20%281%29.PNG) apparirà questa schermata:

![Screenshot creazione import](../../../.gitbook/assets/campiimport.PNG)

La quale mostrerà il contenuto di ogni colonna. Cliccando su ![](../../../.gitbook/assets/avviaimportazione.PNG)  il file viene importato nel modulo _Articoli_.

![Screenshot import appena creato](../../../.gitbook/assets/importazione%20%282%29.PNG)

### Attenzione

{% hint style="warning" %}
Se devi importare un file **CSV** di una **Anagrafica** devi andare ad aggiungere nel file una colonna **Tipologia** specificando il **Tipo di anagrafica\(Agente,Vettore,Cliente,Azienda,Fornitore\)**
{% endhint %}

![Aggiunta campo Tipologia al file CSV](../../../.gitbook/assets/tipologiacliente.PNG)

{% hint style="warning" %}
Non andando a specificare la **Tipologia** nel modulo **Anagrafiche** il campo **Tipo** rimarrà vuoto.

Nell'immagine sottostante il _record_ con **Ragione sociale Test** ha il campo **Tipo** vuoto, mentre nel successivo _record_ è presente, proprio perché è specificata la **Tipologia** nel file **CSV.** 
{% endhint %}

![Anagrafica importata correttamente](../../../.gitbook/assets/importazioneclienteok.PNG)

