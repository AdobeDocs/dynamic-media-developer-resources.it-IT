---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
topic: Dynamic media
uuid: 2f44dc7f-ebed-4c74-b1ea-0b65655059fe
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di zoom con doppio clic o tocco. Se si imposta su <span class="codeph"> none </span>, lo zoom con doppio clic/tocco viene disattivato. Se è impostato su <span class="codeph"> zoom </span>, facendo clic sull'immagine si esegue lo zoom in un passaggio di zoom; CTRL+clic consente di ridurre un passaggio di zoom. Se si imposta <span class="codeph"> reimposta </span>, lo zoom viene reimpostato al livello iniziale con un solo clic sull'immagine. Per <span class="codeph"> zoomReset </span>, viene applicato reset se il fattore di zoom corrente è uguale o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` su computer desktop;  `zoomReset` su dispositivi touch.

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
