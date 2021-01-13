---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
topic: Dynamic media
uuid: 676a13b5-4634-4233-8059-6effed6e2b5d
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
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

## Proprietà {#section-50bcd15223174bb79ce08b31ea03d682}

Facoltativo.

## Predefinito {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` su computer desktop;  `zoomReset` su dispositivi touch.

## Esempio {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
