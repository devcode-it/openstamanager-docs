# Gestione upload

OpenSTAManager presenta una struttura comune per la gestione degli upload da parte dell'utente per il singolo record di un modulo o plugin.

Questa funzione, qualora abilitata per il modulo in utilizzo, si presenta nel seguente modo:

![Screenshot della sezione di gestione degli upload](../.gitbook/assets/uploads.png)

## Struttura interna

Tutti gli upload di OpenSTAManager vengono salvati all'interno della cartella `files/` , suddivisi secondo il nome del modulo cui sono relativi.

{% hint style="info" %}
I file di upload vengono rinominati in modo casuale al fine di evitare una possibile sovrascrittura di file preesistenti, e pertanto non è possibile risalire manualmente a un qualunque file che è stato caricato.
{% endhint %}
