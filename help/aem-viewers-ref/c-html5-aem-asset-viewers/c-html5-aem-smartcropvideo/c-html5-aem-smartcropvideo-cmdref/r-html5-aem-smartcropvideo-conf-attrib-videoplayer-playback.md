---
title: SmartCropVideoPlayer.playback
description: Attributo di configurazione per il visualizzatore video Ritaglio avanzato.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6df94fe7-30ea-42f1-a39e-50219259a098
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Attributo di configurazione per il visualizzatore video Ritaglio avanzato.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> automatico|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Imposta il tipo di riproduzione utilizzato dal visualizzatore. Quando è impostato <span class="codeph"> auto</span>, nella maggior parte dei browser desktop e in tutti i dispositivi iOS, il visualizzatore utilizza video streaming HTML5 in formato HLS. Si basa sulla riproduzione progressiva di HTML5 su alcuni sistemi come i vecchi Internet Explorer e Android™. </p> <p>Se si specifica <span class="codeph"> progressive</span>, il visualizzatore si basa solo sulla riproduzione di HTML5 supportata in modalità nativa dai browser e riproduce il video in modo progressivo su tutti i sistemi. </p> <p>Per ulteriori informazioni sulla selezione della riproduzione in modalità automatica e progressiva, consultare la Guida utente di Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

Ignorato quando il visualizzatore funziona con un video esterno. Consulta [Supporto video esterno]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
