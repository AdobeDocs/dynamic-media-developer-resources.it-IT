---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '180'
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
   <td colname="col2"> <p>Specifica in che modo il componente gestisce le immagini piccole. </p> <p>Se il componente è impostato su <span class="codeph"> 1</span>, l'immagine principale viene ridimensionata in modo che rientri nella vista principale. Inoltre, l’immagine di zoom viene ridimensionata in modo da riempire completamente l’area della finestra a comparsa configurata. </p> <p>Se impostate su <span class="codeph"> 0</span>, le immagini piccole vengono visualizzate alla risoluzione originale e vengono visualizzate centrate nell'area di visualizzazione principale e all'interno della finestra a comparsa. Potete configurare uno spazio bianco aggiuntivo che viene visualizzato attorno all'immagine con una proprietà CSS di sfondo o simile delle classi CSS <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> rispettivamente nella vista principale e nella finestra a comparsa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
