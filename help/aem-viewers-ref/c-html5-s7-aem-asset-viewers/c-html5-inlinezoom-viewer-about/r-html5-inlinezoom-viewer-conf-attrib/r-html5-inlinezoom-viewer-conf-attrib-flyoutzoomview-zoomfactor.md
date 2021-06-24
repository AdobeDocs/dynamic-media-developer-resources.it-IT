---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom in linea
role: Developer,Business Practitioner
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecondariFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica l'ingrandimento dell'immagine per la visualizzazione a comparsa, rispetto alla vista principale. Deve essere un valore intero o a virgola mobile <span class="codeph"> 1.0</span> o superiore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondarioFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> È possibile specificare un fattore secondario facoltativo accessibile toccando o facendo clic sulla vista principale quando l’evidenziazione è attiva. Quando si tocca o fai clic su un secondo pulsante, viene ripristinato il fattore di zoom principale. Un valore di <span class="codeph"> -1</span> disattiva il fattore di zoom secondario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> aumento</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica come il componente gestisce le immagini di piccole dimensioni. </p> <p>Se è impostato su <span class="codeph"> 1</span> il componente ingrandisce l'immagine principale in modo che si adatti alla visualizzazione principale. Inoltre, aumenta l'immagine dello zoom in modo da riempire completamente l'area della finestra a comparsa configurata. </p> <p>Se impostato su <span class="codeph"> 0</span>, le immagini piccole vengono visualizzate con la risoluzione originale e vengono visualizzate centrate nell'area di visualizzazione principale e all'interno della finestra a comparsa. Puoi configurare uno spazio bianco aggiuntivo intorno all’immagine con una proprietà CSS di sfondo o simile delle classi CSS <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> rispettivamente nella vista principale e nella finestra a comparsa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
