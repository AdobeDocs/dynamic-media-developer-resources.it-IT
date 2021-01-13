---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
topic: Dynamic media
uuid: 11458300-4a1b-4623-8ea1-db804daab3cf
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p> Configura il numero di azioni di zoom in e zoom out necessarie per aumentare o ridurre la risoluzione di un fattore di due. La modifica della risoluzione per ogni azione di zoom è di 2^1 per passaggio. Impostare su <span class="codeph"> 0</span> per eseguire lo zoom a risoluzione completa con una singola azione di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limit</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica la risoluzione di zoom massima, relativa all’immagine a risoluzione piena. Il valore predefinito è <span class="codeph"> 1.0</span>, che non consente lo zoom oltre la risoluzione completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-636d35a4791447039f1902973f568320}

Facoltativo.

## Predefinito {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## Esempio {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
