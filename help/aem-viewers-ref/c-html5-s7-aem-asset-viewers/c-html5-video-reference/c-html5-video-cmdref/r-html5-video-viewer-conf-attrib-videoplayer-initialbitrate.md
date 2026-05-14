---
title: VideoPlayer.initialbitrate
description: Attributo di configurazione per Visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
TQID: 'https://experienceleague.adobe.com/Z1oVEpUm58QxYopF3XYd66HXHtzLPOrqea2YKzedD0U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Attributo di configurazione per Visualizzatore video.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`valore`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valore </span> </p> </td> 
   <td colname="col2"> <p>Imposta il bitrate video (in kilobit al secondo o Kbps) utilizzato per la riproduzione iniziale del video sui desktop. </p> <p>Se questo valore di bitrate non esiste nel set di video adattivi, il lettore video avvia il video che ha il bitrate inferiore più prossimo. </p> <p>Se è impostato su <span class="codeph"> 0 </span>, il lettore video inizia dal bitrate più basso possibile. Applicabile solo per i sistemi che non dispongono del supporto nativo per HTML5 HLS video (che sono browser Firefox, Chrome e Internet Explorer 11 su Windows 10) e quando la modalità di riproduzione è impostata su <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
