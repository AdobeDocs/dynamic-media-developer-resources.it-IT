---
description: Riferimento API JavaScript per il visualizzatore carosello.
seo-description: Riferimento API JavaScript per il visualizzatore carosello.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 770cbb87-af86-48dc-88a0-e74f6716f545
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---


# setAsset{#setasset}

Riferimento API JavaScript per il visualizzatore carosello.

` setAsset( *`asset`*)`

Imposta la nuova risorsa. Potete chiamare questo parametro in qualsiasi momento, prima o dopo `init()`. Se viene chiamato dopo `init()`, il visualizzatore scambia la risorsa in fase di esecuzione.

Vedere anche [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nuovo ID risorsa. </p> <p>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Riferimento immagine singolo:

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```

