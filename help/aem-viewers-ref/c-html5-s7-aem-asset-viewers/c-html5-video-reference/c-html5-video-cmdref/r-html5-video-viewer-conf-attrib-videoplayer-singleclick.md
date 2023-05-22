---
title: VideoPlayer.singleclick
description: Attributo di configurazione per Visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Attributo di configurazione per Visualizzatore video.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

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
