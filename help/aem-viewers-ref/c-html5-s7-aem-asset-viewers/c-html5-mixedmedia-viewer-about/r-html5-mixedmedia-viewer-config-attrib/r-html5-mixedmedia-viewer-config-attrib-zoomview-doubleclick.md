---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e87981f8-8174-432a-89ea-fae74d0584ad
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di doppio clic/tocco per lo zoom. Impostazione su <span class="codeph"> nessuno </span> disabilita lo zoom con doppio clic o tocco. Se impostato su <span class="codeph"> zoom </span> facendo clic sull'immagine si ingrandisce un passaggio di zoom; CTRL+clic consente di ingrandire un passaggio di zoom. Impostazione su <span class="codeph"> reset </span> fa sì che un singolo clic sull'immagine reimposti lo zoom al livello di zoom iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il reset se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` su computer desktop; `zoomReset` su dispositivi touch.

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
