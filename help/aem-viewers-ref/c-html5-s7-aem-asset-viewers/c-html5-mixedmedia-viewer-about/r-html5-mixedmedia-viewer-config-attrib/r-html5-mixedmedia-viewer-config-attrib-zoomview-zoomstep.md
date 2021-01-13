---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
topic: Dynamic media
uuid: 914091e0-f026-423c-8c33-86a0284ac600
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '78'
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

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
