---
description: Attributo di configurazione per il visualizzatore video.
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video
role: Developer,Business Practitioner
exl-id: 7f9f1bfe-c68f-4ad4-a4a3-e0a8952e07af
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Attributo di configurazione per il visualizzatore video.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Specifica (in kbit per secondo o kbps) il bit rate video desiderato da riprodurre da un set video adattivo nel caso in cui il sistema corrente non supporti la riproduzione video adattiva. </p> <p>Il componente raccoglie il flusso video con il bitrate più vicino possibile (ma non superiore) al valore specificato. Se tutti i flussi video nel set video adattivo hanno una qualità superiore rispetto al valore specificato, la logica sceglie il bitrate con la qualità più bassa. </p> </td> 
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
