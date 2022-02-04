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
ht-degree: 4%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di tocco/clic singolo per lo zoom. Impostazione su <span class="codeph"> nessuno </span> disabilita lo zoom con un solo clic o tocco. Se impostato su <span class="codeph"> girare </span> facendo clic sull'immagine si ingrandisce un passaggio di zoom; CTRL+clic consente di ingrandire un passaggio di zoom. Impostazione su <span class="codeph"> reset </span> fa sì che un singolo clic sull'immagine reimposti lo zoom al livello di rotazione iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il reset se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` su computer desktop; `none` su dispositivi touch.

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
