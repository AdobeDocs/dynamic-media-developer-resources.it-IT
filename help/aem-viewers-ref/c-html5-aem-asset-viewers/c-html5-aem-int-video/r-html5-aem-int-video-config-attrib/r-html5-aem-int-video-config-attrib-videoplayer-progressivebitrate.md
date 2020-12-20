---
description: Attributo di configurazione per il visualizzatore video interattivo.
seo-description: Attributo di configurazione per il visualizzatore video interattivo.
seo-title: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic media
uuid: 72438e50-29fc-484f-8a3b-be8909e7864f
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Attributo di configurazione per il visualizzatore video interattivo.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Specifica in kbit per secondo (o kbps) il bitrate video desiderato da riprodurre da un set video adattivo nel caso in cui il sistema corrente non supporti la riproduzione video adattiva. </p> <p>Il componente riproduce il flusso video con il bitrate più vicino possibile (ma non superiore) al valore specificato. Se tutti i flussi video del set video adattivo hanno una qualità superiore rispetto al valore specificato, la logica sceglie il bitrate con la qualità più bassa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```

