---
description: Riferimento API JavaScript per il visualizzatore di file multimediali diversi.
seo-description: Riferimento API JavaScript per il visualizzatore di file multimediali diversi.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 46db0ce3-fd70-4577-92ed-e7d2d15e0dab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParams{#setparams}

Riferimento API JavaScript per il visualizzatore di file multimediali diversi.

` setParams( *`params`*)`

Imposta uno o più parametri su un valore specificato. La sintassi dell&#39;argomento metodo è identica a una stringa di query URL. Rappresenta cioè coppie nome=valore separate con `&`. Come in una stringa di query, i nomi e i valori sono codificati in percentuale con UTF8. Prima di chiamare `init()`, è necessario chiamare questo parametro. Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono trasmesse con l&#39;oggetto `config` JSON al costruttore.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=coppie di parametri di valore separate da <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomstep=2,3&ZoomView.iscommand=op_sharpen%3d1")
```

