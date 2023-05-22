---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ded8168e-08f7-4bc0-bb8a-624bac82759e
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 3%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`passaggio`*[, *`limit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passaggio</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura il numero di azioni di zoom in/zoom out necessarie per aumentare/ridurre la risoluzione di un fattore di 2. La modifica della risoluzione per ogni azione di zoom è 2^1 per incremento. Imposta su <span class="codeph"> 0</span> per effettuare lo zoom a risoluzione massima con una singola azione di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> limit</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica la risoluzione di zoom massima, relativa alla risoluzione massima dell'immagine. Il valore predefinito è <span class="codeph"> 1,0</span>, che non consente lo zoom oltre la risoluzione massima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-50bcd15223174bb79ce08b31ea03d682}

Facoltativo.

## Predefinito {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## Esempio {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
