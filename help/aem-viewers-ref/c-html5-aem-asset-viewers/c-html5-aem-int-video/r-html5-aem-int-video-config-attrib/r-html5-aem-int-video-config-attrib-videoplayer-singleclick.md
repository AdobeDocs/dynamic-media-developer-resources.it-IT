---
description: Attributo di configurazione per il visualizzatore video interattivo.
seo-description: Attributo di configurazione per il visualizzatore video interattivo.
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic media
uuid: 5b387eb6-1e09-4506-beea-3f1cf337cb9d
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

Attributo di configurazione per il visualizzatore video interattivo.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura del singolo clic/tocco per attivare/disattivare la riproduzione/pausa. Se si imposta su <span class="codeph"> none</span> , il tocco o il clic singolo viene disattivato per la riproduzione o la pausa. Se è impostato su <span class="codeph"> Pausa</span> , facendo clic sul video si passa dalla riproduzione alla pausa. Su alcuni dispositivi è possibile utilizzare i controlli nativi. In questo caso, un <span class="codeph"> comportamento con un solo clic</span> è disabilitato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`playPause`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```

