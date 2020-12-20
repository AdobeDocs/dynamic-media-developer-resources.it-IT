---
description: Attributo di configurazione per il visualizzatore video.
seo-description: Attributo di configurazione per il visualizzatore video.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 5ab7a322-9de0-4a26-95be-b9b2ff8e5a84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

Attributo di configurazione per il visualizzatore video.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Imposta il tipo di riproduzione utilizzato dal visualizzatore. Quando si imposta <span class="codeph"> auto</span>, nella maggior parte dei browser desktop e in tutti i dispositivi iOS, il visualizzatore utilizza lo streaming video HTML5 in formato HLS. Riprende la riproduzione HTML5 progressiva su alcuni sistemi come Internet Explorer e Android. </p> <p>Se si specifica <span class="codeph"> progressive</span>, il visualizzatore utilizza solo la riproduzione HTML5 come supportata in modo nativo dai browser e riproduce progressivamente il video su tutti i sistemi. </p> <p>Per ulteriori informazioni sulla selezione della riproduzione nelle modalità automatica e progressiva, consultate la guida utente dell’SDK per visualizzatori. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

Ignorato quando il visualizzatore funziona con video esterni. Consultate [Supporto per video esterni](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

