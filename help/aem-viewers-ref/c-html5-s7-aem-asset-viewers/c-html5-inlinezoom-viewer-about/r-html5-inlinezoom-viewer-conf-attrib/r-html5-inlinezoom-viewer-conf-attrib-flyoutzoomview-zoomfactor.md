---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondarioFactor`*][, *`aumento`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica l'ingrandimento dell'immagine per la visualizzazione a comparsa, rispetto alla vista principale. Deve essere un valore intero o a virgola mobile <span class="codeph"> 1,0</span> o superiore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondarioFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> È possibile specificare un fattore secondario facoltativo accessibile toccando o facendo clic sulla vista principale quando l’evidenziazione è attiva. Quando si tocca o fai clic su un secondo pulsante, viene ripristinato il fattore di zoom principale. Un valore di <span class="codeph"> -1</span> disabilita il fattore di zoom secondario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> aumento</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica come il componente gestisce le immagini di piccole dimensioni. </p> <p>Se impostato su <span class="codeph"> 1</span> il componente ingrandisce l’immagine principale in modo che si adatti alla vista principale. Inoltre, aumenta l'immagine dello zoom in modo da riempire completamente l'area della finestra a comparsa configurata. </p> <p>Se impostato su <span class="codeph"> 0</span>, le immagini di piccole dimensioni vengono visualizzate con la risoluzione originale e il display centrato nell'area di visualizzazione principale e all'interno della finestra a comparsa. Puoi configurare uno spazio bianco aggiuntivo intorno all’immagine con uno sfondo o una proprietà CSS simile del <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> Classi CSS nella vista principale e nella finestra a comparsa, rispettivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
