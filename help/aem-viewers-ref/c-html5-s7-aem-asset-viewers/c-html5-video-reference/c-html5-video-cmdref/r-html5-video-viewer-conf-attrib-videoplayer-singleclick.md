---
title: VideoPlayer.singleclick
description: Attributo di configurazione per il visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Attributo di configurazione per il visualizzatore video.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura di un singolo clic/tocco per attivare/disattivare la riproduzione/pausa. Impostazione su <span class="codeph"> nessuno</span> disabilita il tocco o il clic singolo per riprodurre/mettere in pausa. Se impostato su <span class="codeph"> playPause</span>, facendo clic sul video si passa dalla riproduzione alla messa in pausa del video. Su alcuni dispositivi è possibile utilizzare controlli nativi. In tal caso, <span class="codeph"> singleclick</span> il comportamento è disabilitato. </p> </td> 
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
