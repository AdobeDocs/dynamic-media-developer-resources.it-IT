---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: 18c5c21d-af31-4b1c-ab8b-c04d08650123
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di tocco/clic singolo per lo zoom. Impostando su <span class="codeph"> none </span> si disattiva lo zoom con un solo clic o tocco. Se è impostato su <span class="codeph"> zoom </span> facendo clic sull'immagine si ingrandisce un solo passaggio di zoom; CTRL+clic consente di ingrandire un passaggio di zoom. Impostando su <span class="codeph"> reset </span> si reimposta un singolo clic sull'immagine per reimpostare lo zoom al livello iniziale di rotazione. Per <span class="codeph"> zoomReset </span>, viene applicato il reset se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` su computer desktop;  `none` su dispositivi touch.

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
