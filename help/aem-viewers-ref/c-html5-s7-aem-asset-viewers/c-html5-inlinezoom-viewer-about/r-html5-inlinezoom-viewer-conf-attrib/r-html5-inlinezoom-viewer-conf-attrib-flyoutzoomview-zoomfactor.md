---
title: FattoreZoomVisualizzazione.zoom
description: FattoreZoomVisualizzazione.zoom
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
TQID: 'https://experienceleague.adobe.com/9J-cksIEU-w-jRL4PN0dklGMWCpu0c74oSMdw-AX2IQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 1%

---

# FattoreZoomVisualizzazione.zoom{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica l'ingrandimento dell'immagine per la visualizzazione a comparsa, rispetto alla visualizzazione principale. Deve essere un numero intero o un valore a virgola mobile <span class="codeph"> 1,0</span> o maggiore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fattore secondario</span> </span> </p> </td> 
   <td colname="col2"> <p> È possibile specificare un fattore secondario facoltativo accessibile facendo clic o toccando la vista principale quando l'evidenziazione è attiva. Toccando o facendo clic una seconda volta si ritorna al fattore di zoom primario. Il valore <span class="codeph"> -1</span> disattiva il fattore di zoom secondario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica come il componente gestisce le immagini di piccole dimensioni. </p> <p>Se è impostato su <span class="codeph"> 1</span>, il componente esegue l'upscaling dell'immagine principale in modo che rientri nella visualizzazione principale. Inoltre, esegue l'upscaling dell'immagine di zoom in modo da riempire completamente l'area configurata della finestra a comparsa. </p> <p>Se è impostato su <span class="codeph"> 0</span>, le immagini di piccole dimensioni vengono visualizzate alla risoluzione originale e centrate nell'area di visualizzazione principale e all'interno della finestra a comparsa. È possibile configurare uno spazio vuoto aggiuntivo intorno all'immagine con uno sfondo o una proprietà CSS simile delle classi CSS <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> rispettivamente nella visualizzazione principale e nella finestra a comparsa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
