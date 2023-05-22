---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di clic/tocco per eseguire lo zoom. Impostazione di <span class="codeph"> nessuno </span> disattiva lo zoom con clic/tocco singolo. Se impostato su <span class="codeph"> zoom </span> se si fa clic sull'immagine, questa si ingrandisce di un livello; se si fa clic tenendo premuto CTRL l'immagine si riduce di un livello. Impostazione di <span class="codeph"> ripristina </span> fa in modo che, con un singolo clic, l'immagine ripristini il livello di zoom iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il ripristino se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`zoomReset` - su computer desktop; `none` sui dispositivi touch.

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
