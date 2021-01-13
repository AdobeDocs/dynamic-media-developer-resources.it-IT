---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 8c4e6bf8-0238-470b-9fbe-262eb17f8f3b
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`PrimaryFactorsecondarioFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mainFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica l’ingrandimento dell’immagine per la visualizzazione a comparsa, rispetto alla vista principale. Deve essere un numero intero o un valore a virgola mobile <span class="codeph"> 1.0</span> o superiore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondariaFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> È possibile specificare un fattore secondario facoltativo accessibile toccando o facendo clic sulla vista principale quando l'evidenziazione è attiva. Toccando o facendo clic una seconda volta viene ripristinato il fattore di zoom principale. Un valore di <span class="codeph"> -1</span> disattiva il fattore di zoom secondario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica in che modo il componente gestisce le immagini piccole. </p> <p>Se il componente è impostato su <span class="codeph"> 1</span>, l'immagine principale viene ridimensionata in modo che rientri nella vista principale. Inoltre, l’immagine di zoom viene ridimensionata in modo da riempire completamente l’area della finestra a comparsa configurata. </p> <p>Se impostate su <span class="codeph"> 0</span>, le immagini piccole vengono visualizzate alla risoluzione originale e vengono visualizzate centrate nell'area di visualizzazione principale e all'interno della finestra a comparsa. Potete configurare uno spazio bianco aggiuntivo intorno all'immagine con una proprietà CSS di sfondo o simile delle classi CSS <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> rispettivamente nella vista principale e nella finestra a comparsa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
