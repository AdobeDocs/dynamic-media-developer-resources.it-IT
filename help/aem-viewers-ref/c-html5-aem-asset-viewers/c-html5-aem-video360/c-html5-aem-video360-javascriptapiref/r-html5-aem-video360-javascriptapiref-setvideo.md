---
description: Riferimento API JavaScript per il visualizzatore video360
solution: Experience Manager
title: setVideo
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video VR 360
role: Developer,Business Practitioner
exl-id: e1894d96-6f37-4e34-a709-5b0121bd0696
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# setVideo{#setvideo}

Riferimento API JavaScript per il visualizzatore video360

`setVideo(videoUrl)`

Imposta il nuovo video esterno. Può essere chiamato in qualsiasi momento, sia prima che dopo `init()`. Se viene chiamato dopo `init()`, il visualizzatore scambia il video in fase di esecuzione.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parametri {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl  </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} un URL assoluto al nuovo video. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```
