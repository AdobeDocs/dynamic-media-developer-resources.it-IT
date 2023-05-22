---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di clic/tocco per eseguire lo zoom. Impostazione di <span class="codeph"> nessuno </span> disattiva lo zoom con clic/tocco singolo. Se impostato su <span class="codeph"> girare </span> se si fa clic sull'immagine, questa si ingrandisce di un livello; se si fa clic tenendo premuto CTRL l'immagine si riduce di un livello. Impostazione di <span class="codeph"> ripristina </span> fa in modo che, con un singolo clic sull’immagine, lo zoom torni al livello di rotazione iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il ripristino se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` Su computer desktop; `none` sui dispositivi touch.

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
