---
description: Riferimento API JavaScript per visualizzatore zoom in linea.
seo-description: Riferimento API JavaScript per visualizzatore zoom in linea.
seo-title: setParams
solution: Experience Manager
title: setParams
uuid: 50fde4b0-2fd8-4341-bb2f-b1785f82ebc1
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom in linea
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 1%

---


# setParams{#setparams}

Riferimento API JavaScript per visualizzatore zoom in linea.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value coppie di parametri separate con  <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta uno o più parametri su un valore specificato. La sintassi dell&#39;argomento del metodo è identica a una stringa di interrogazione URL. In altre parole, rappresenta coppie nome=valore separate da `&`. Come in una stringa di query, i nomi e i valori sono codificati in percentuale utilizzando UTF8. Prima di chiamare `init()`, è necessario chiamare questo parametro. Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono passate con l’oggetto JSON `config` al costruttore.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```

