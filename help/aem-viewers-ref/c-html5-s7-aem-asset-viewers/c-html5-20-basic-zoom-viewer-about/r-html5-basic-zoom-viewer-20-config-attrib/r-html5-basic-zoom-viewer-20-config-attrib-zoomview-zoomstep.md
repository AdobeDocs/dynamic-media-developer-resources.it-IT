---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
uuid: 948b154a-250c-41a8-967b-d199ddb6e5e1
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 4%

---


# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> step</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura il numero di azioni di zoom in e zoom out necessarie per aumentare o ridurre la risoluzione di un fattore di due. La modifica della risoluzione per ogni azione di zoom è di 2^1 per passo. Impostare su <span class="codeph"> 0</span> per ingrandire la risoluzione completa con una singola azione di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> limite</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica la risoluzione massima dello zoom rispetto all'immagine a risoluzione piena. Il valore predefinito è <span class="codeph"> 1.0</span>, che non consente lo zoom oltre la risoluzione completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-50bcd15223174bb79ce08b31ea03d682}

Facoltativo.

## Predefinito {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## Esempio {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
