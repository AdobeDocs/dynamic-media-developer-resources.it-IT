---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
topic: Dynamic media
uuid: bc68fc0a-94bf-42b3-a386-e0a248e8445c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 5%

---


# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p> Configura le azioni di zoom in e zoom out necessarie per aumentare o ridurre la risoluzione di un fattore di due. La modifica della risoluzione per ogni azione di zoom è di 2^1 per passaggio. Impostare su <span class="codeph"> 0</span> per eseguire lo zoom a risoluzione completa con una singola azione di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limit</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica la risoluzione di zoom massima, relativa all’immagine a risoluzione piena. Il valore predefinito è <span class="codeph"> 1.0</span>, che non consente lo zoom oltre la risoluzione completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,1`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`
