---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: bcd153f3-7a87-4e8f-825b-fc4a136de1dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 3%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`passaggio`*[, *`limit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> passaggio</span></span> </p> </td> 
   <td colname="col2"> <p> Configura il numero di azioni di zoom in/zoom out necessarie per aumentare/ridurre la risoluzione di un fattore di 2. La modifica della risoluzione per ogni azione di zoom è 2^1 per incremento. Imposta su <span class="codeph"> 0</span> per effettuare lo zoom a risoluzione massima con una singola azione di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limit</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica la risoluzione di zoom massima, relativa alla risoluzione massima dell'immagine. Il valore predefinito è <span class="codeph"> 1,0</span>, che non consente lo zoom oltre la risoluzione massima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,1`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`
