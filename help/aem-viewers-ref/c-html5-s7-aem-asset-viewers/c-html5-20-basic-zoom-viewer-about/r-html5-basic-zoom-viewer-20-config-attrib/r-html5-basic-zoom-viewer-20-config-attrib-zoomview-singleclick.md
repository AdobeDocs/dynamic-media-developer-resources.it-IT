---
description: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---


# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di tocco/clic singolo per lo zoom. Impostando su <span class="codeph"> none </span> si disattiva lo zoom con un solo clic o tocco. Se è impostato su <span class="codeph"> zoom </span> facendo clic sull'immagine si ingrandisce un solo passaggio di zoom; CTRL+clic consente di ingrandire un passaggio di zoom. Se si imposta il valore <span class="codeph"> reset </span> , si farà clic sull'immagine per ripristinare lo zoom al livello iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il reset se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-50bcd15223174bb79ce08b31ea03d682}

Facoltativo.

## Predefinito {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` su computer desktop;  `none` su dispositivi touch.

## Esempio {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
