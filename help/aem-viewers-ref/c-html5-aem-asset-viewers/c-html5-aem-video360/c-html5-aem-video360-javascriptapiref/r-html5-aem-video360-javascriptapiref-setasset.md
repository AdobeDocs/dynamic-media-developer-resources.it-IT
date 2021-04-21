---
description: Riferimento API JavaScript per il visualizzatore Video360.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: 1fcd7dbe-d122-4501-92f4-3ce93a94a933
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 4%

---

# setAsset{#setasset}

Riferimento API JavaScript per il visualizzatore Video360.

`setAsset(asset)`

Imposta la nuova risorsa. Puoi chiamare questo parametro in qualsiasi momento, prima o dopo `init()`. Se viene chiamato dopo `init()`, il visualizzatore scambia la risorsa in fase di runtime.

Vedere anche [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nuovo ID risorsa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Viewers/space_station_360-AVS")
```
