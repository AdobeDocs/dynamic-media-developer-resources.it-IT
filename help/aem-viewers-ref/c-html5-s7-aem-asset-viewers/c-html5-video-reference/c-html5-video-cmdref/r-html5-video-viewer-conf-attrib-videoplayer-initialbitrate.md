---
description: Attributo di configurazione per il visualizzatore video.
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Attributo di configurazione per il visualizzatore video.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value  </span> </p> </td> 
   <td colname="col2"> <p>Imposta i bit in bit/bit in bitrate video per secondi o kbps-utilizzati per la riproduzione iniziale del video sui desktop. </p> <p>Se questo valore di bitrate non esiste nel set video adattivo, il lettore video avvia il video con il bitrate più basso successivo. </p> <p>Se è impostato su <span class="codeph"> 0 </span>, il lettore video inizia dal bitrate più basso possibile. Applicabile solo ai sistemi che non dispongono del supporto nativo per video HTML5 HLS (che sono browser Firefox, Chrome e Internet Explorer 11 su Windows 10) e quando la modalità di riproduzione è impostata su <span class="codeph"> auto </span>. </p> </td> 
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

