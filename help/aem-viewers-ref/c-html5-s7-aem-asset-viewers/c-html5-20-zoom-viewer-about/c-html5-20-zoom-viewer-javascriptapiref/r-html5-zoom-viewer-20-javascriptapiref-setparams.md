---
title: setParams
description: Riferimento API JavaScript per il visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: af31b5eb-2051-4f4c-861d-67ada3248fd6
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 2%

---

# setParams{#setparams}

Riferimento API JavaScript per il visualizzatore video.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> coppie di parametri name=value separate da <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta uno o più parametri su un valore specificato. La sintassi dell&#39;argomento del metodo è identica a una stringa di interrogazione URL. Cioè, rappresenta coppie nome=valore separate da `&`. Come in una stringa di query, i nomi e i valori sono codificati in percentuale utilizzando UTF8. Prima di chiamare `init()`, questo parametro deve essere chiamato.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore sono state passate con `config` Oggetto JSON al costruttore.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```
