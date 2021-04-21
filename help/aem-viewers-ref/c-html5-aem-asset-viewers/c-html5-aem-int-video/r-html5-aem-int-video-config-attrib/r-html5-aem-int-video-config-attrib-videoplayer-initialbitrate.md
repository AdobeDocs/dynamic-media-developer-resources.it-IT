---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Attributo di configurazione per Visualizzatore video interattivo.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Imposta il bitrate video (in kbit al secondo o kbps) utilizzato per la riproduzione iniziale del video su un desktop. </p> <p>Se questo valore di bitrate non esiste nel set video adattivo, il lettore video inizia con il video con il bitrate successivo inferiore. </p> <p>Se è impostato su <span class="codeph"> 0</span>, il lettore video inizia dal bitrate più basso possibile. </p> <p>Applicabile solo ai sistemi che non dispongono del supporto nativo per video HTML5 HLS (come i browser Firefox, Chrome e Internet Explorer 11 su Windows 10) e quando la modalità di riproduzione è impostata su Automatico. </p> </td> 
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
