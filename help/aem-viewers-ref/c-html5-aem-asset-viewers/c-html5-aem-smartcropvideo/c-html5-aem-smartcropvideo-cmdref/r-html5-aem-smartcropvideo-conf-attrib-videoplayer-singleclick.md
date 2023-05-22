---
title: SmartCropVideoPlayer.singleclick
description: Attributo di configurazione per il visualizzatore video Ritaglio avanzato.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: f48f0866-4eb7-46c5-a7f5-457df7a568e7
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

Attributo di configurazione per il visualizzatore video Ritaglio avanzato.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura di clic/tocco per riprodurre e mettere in pausa. Impostazione di <span class="codeph"> nessuno</span> disabilita il clic/tocco per riprodurre/mettere in pausa. Se impostato su <span class="codeph"> playPause</span>, quando si fa clic sul video, la riproduzione viene interrotta e il video interrotto. Su alcuni dispositivi è possibile utilizzare i controlli nativi. In tal caso: <span class="codeph"> singleclick</span> il comportamento è disabilitato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```
