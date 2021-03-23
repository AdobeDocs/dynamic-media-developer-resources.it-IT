---
description: Attributo di configurazione per il visualizzatore video.
seo-description: Attributo di configurazione per il visualizzatore video.
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
uuid: df669b2e-31da-4de0-b480-e54402c9545c
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

Attributo di configurazione per il visualizzatore video.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura di un singolo clic/tocco per attivare/disattivare la riproduzione/pausa. Impostando su <span class="codeph"> none</span> si disattiva il tocco o il clic singolo per riprodurre/mettere in pausa. Se è impostato su <span class="codeph"> playPause</span>, facendo clic sul video si passa dalla riproduzione alla messa in pausa. Su alcuni dispositivi è possibile utilizzare controlli nativi. In questo caso, il comportamento <span class="codeph"> singleclick</span> è disabilitato. </p> </td> 
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

