---
title: VideoPlayer.initialbitrate
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
TQID: 'https://experienceleague.adobe.com/UND2NsxA0NTd9-AIt-QcrYA42SPW49wb4KEeEMTd-no'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Attributo di configurazione per Visualizzatore video interattivo.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`valore`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Valore <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p> Imposta il bitrate video (in kilobit al secondo o Kbps) utilizzato per la riproduzione iniziale del video su un desktop. </p> <p>Se questo valore di bitrate non esiste nel set di video adattivi, il lettore video inizia con il video che ha il bitrate inferiore successivo. </p> <p>Se è impostato su <span class="codeph"> 0</span>, il lettore video inizia dal bitrate più basso possibile. </p> <p>Applicabile solo per i sistemi che non dispongono di supporto nativo per i video HTML5 HLS (come i browser Firefox, Chrome e Internet Explorer 11 su Windows 10) e quando la modalità di riproduzione è impostata su auto. </p> </td> 
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
