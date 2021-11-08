---
title: SmartCropVideoPlayer.playback
description: Attributo di configurazione per Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Attributo di configurazione per Smart Crop Video Viewer.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> automatico|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Imposta il tipo di riproduzione utilizzato dal visualizzatore. Quando <span class="codeph"> auto</span> nella maggior parte dei browser desktop e in tutti i dispositivi iOS, il visualizzatore utilizza lo streaming video HTML5 in formato HLS. Ritorna alla riproduzione progressiva HTML5 su alcuni sistemi come Internet Explorer e Android™. </p> <p>Se <span class="codeph"> progressivo</span> è specificato, il visualizzatore si basa solo sulla riproduzione di HTML5 come supportato in formato nativo dai browser e riproduce progressivamente i video su tutti i sistemi. </p> <p>Per ulteriori informazioni sulla selezione della riproduzione nelle modalità automatica e progressiva, consulta la Guida utente dell’SDK per visualizzatori. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

Ignorato quando il visualizzatore funziona con video esterno. Vedi [Supporto video esterno]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
