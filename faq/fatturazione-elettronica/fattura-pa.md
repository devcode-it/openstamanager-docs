# Split payment e reverse charge

{% hint style="info" %}
La pubblica amministrazione richiede **split payment** o **reverse charge**. Come gestire questi due parametri in **OpenSTAManager**?
{% endhint %}

## Split payment

Creando una fattura di vendita è possibile abilitare lo **split payment** spuntando la casella sotto indicata.

![](../../.gitbook/assets/splitpayment.png)

Così facendo nella tabella **Righe** il **Totale** sarà annesso **IVA** mentre il **Netto a pagare** è senza **IVA** perché sarà la pubblica amministrazione a contribuire l'imposta relativa alla transazione**,** come nell'esempio che segue:

![](../../.gitbook/assets/righesplitpayment.png)

## Reverse charge

Il reverse charge è applicabile ad una **Riga** selezionandolo nel campo **Iva,** come nell'esempio che segue:

![](../../.gitbook/assets/n6.png)

Il riferimento normativo del _**reverse charge**_ IVA in Italia è rappresentato dall'_articolo 17_, commi 5 e 6.

Quindi, per applicare il **reverse charge** andrò a selezionare Art.17,6, ottenendo così il seguente risultato:

![](../../.gitbook/assets/righen6.png)

Si può quindi notare che non viene applicata l'**IVA** al secondo _record_ .

### Particolarità

Nella creazione di un'anagrafica **Cliente** è possibile abilitare lo **split payment,**così facendo, ogni qualvolta creo una fattura verso quel cliente, il campo **split payment** sarà già spuntato.

![Split payment spuntato in Anagrafica](../../.gitbook/assets/splitpaymentanagrafica.png)

![Split payment automaticamente spuntato nella fattura di vendita](../../.gitbook/assets/splitpaymentflag.png)

