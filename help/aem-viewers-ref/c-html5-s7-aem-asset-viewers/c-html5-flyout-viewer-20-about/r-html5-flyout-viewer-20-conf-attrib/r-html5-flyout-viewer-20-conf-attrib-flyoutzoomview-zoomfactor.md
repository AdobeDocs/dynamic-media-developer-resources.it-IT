---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
feature: Dynamic Media Classic,Visualizzatori,SDK/API,A comparsa
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '188'
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
   <td colname="col2"> <p>Specifica come il componente gestisce le immagini di piccole dimensioni. </p> <p>Se è impostato su <span class="codeph"> 1</span> il componente ingrandisce l'immagine principale in modo che si adatti alla visualizzazione principale. Inoltre, aumenta l'immagine dello zoom in modo da riempire completamente l'area della finestra a comparsa configurata. </p> <p>Se impostato su <span class="codeph"> 0</span>, le immagini piccole vengono visualizzate con la risoluzione originale e vengono visualizzate centrate nell'area di visualizzazione principale e all'interno della finestra a comparsa. È possibile configurare uno spazio bianco aggiuntivo visualizzato intorno all'immagine con uno sfondo o una proprietà CSS simile delle classi CSS <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> rispettivamente nella vista principale e nella finestra a comparsa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
