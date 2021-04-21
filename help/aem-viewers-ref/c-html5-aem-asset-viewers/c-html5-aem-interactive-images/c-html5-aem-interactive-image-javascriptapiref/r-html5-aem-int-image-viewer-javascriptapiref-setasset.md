---
description: Riferimento API JavaScript per il visualizzatore di immagini video.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: e5f88bc9-a880-45eb-9554-57e185937d29
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 3%

---

# setAsset{#setasset}

Riferimento API JavaScript per il visualizzatore di immagini video.

` setAsset( *`asset`*)`

Imposta la nuova risorsa. Puoi chiamare questo parametro in qualsiasi momento, prima o dopo `init()`. Se viene chiamato dopo `init()`, il visualizzatore scambia la risorsa in fase di runtime.

Vedere anche [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> risorsa</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nuovo ID risorsa. </p> <p>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Riferimento immagine singolo:

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```
