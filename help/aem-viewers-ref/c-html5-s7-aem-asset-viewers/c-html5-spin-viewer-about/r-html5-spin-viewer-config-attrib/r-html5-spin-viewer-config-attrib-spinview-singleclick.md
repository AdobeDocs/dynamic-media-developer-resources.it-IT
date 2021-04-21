---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di tocco/clic singolo per lo zoom. Impostando su <span class="codeph"> none </span> si disattiva lo zoom con un solo clic o tocco. Se è impostato su <span class="codeph"> centrifuga </span> facendo clic sull'immagine si ingrandisce un solo passaggio di zoom; CTRL+clic consente di ingrandire un passaggio di zoom. Impostando su <span class="codeph"> reset </span> si reimposta un singolo clic sull'immagine per reimpostare lo zoom al livello iniziale di rotazione. Per <span class="codeph"> zoomReset </span>, viene applicato il reset se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` su computer desktop;  `none` su dispositivi touch.

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
