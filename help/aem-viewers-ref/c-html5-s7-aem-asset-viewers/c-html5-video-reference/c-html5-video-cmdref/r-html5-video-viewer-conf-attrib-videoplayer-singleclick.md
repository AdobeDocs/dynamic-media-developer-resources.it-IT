---
description: Attributo di configurazione per il visualizzatore video.
seo-description: Attributo di configurazione per il visualizzatore video.
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic media
uuid: df669b2e-31da-4de0-b480-e54402c9545c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

Attributo di configurazione per il visualizzatore video.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span></span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura del singolo clic/tocco per attivare/disattivare la riproduzione/pausa. Se si imposta su <span class="codeph"> none</span> , il tocco o il clic singolo viene disattivato per la riproduzione o la pausa. Se è impostato su <span class="codeph"> Pausa</span>, facendo clic sul video si passa dalla riproduzione alla messa in pausa. In alcuni dispositivi è possibile utilizzare i controlli nativi. In tal caso, <span class="codeph"> il comportamento di un singolo clic</span> è disabilitato. </p> </td> 
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

