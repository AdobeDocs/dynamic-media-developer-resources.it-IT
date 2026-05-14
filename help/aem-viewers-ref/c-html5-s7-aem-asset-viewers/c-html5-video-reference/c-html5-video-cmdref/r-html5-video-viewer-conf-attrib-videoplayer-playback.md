---
title: VideoPlayer.playback
description: Attributo di configurazione per Visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
TQID: 'https://experienceleague.adobe.com/kWCkzBjr6vJAyCk6PareJcg8AfwNvm2gNcEC5BpZXxE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

Attributo di configurazione per Visualizzatore video.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

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

Ignorato quando il visualizzatore funziona con un video esterno. Consulta [Supporto video esterno](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
