---
description: Riferimento API JavaScript per il visualizzatore a comparsa.
seo-description: Riferimento API JavaScript per il visualizzatore a comparsa.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 12a513d3-32a9-411d-965f-f0eaf553d98d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 1%

---


# setParams{#setparams}

Riferimento API JavaScript per il visualizzatore a comparsa.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=valore, coppie di parametri separate da  <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta uno o più parametri su un valore specificato. La sintassi dell&#39;argomento metodo è identica a una stringa di query URL. Rappresenta cioè coppie nome=valore separate da `&`. Come in una stringa di query, i nomi e i valori sono codificati in percentuale con UTF8. Prima di chiamare `init()`, questo parametro deve essere chiamato. Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono trasmesse con l&#39;oggetto JSON `config` al costruttore.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```

