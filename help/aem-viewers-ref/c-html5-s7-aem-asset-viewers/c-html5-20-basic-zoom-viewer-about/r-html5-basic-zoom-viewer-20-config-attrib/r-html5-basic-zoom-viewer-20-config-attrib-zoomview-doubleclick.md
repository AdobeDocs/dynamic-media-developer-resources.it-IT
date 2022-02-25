---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 38c90d7f-ddbc-4123-b90d-02f9cabd785c
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
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

## Proprietà {#section-50bcd15223174bb79ce08b31ea03d682}

Facoltativo.

## Predefinito {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` su computer desktop; `zoomReset` su dispositivi touch.

## Esempio {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
