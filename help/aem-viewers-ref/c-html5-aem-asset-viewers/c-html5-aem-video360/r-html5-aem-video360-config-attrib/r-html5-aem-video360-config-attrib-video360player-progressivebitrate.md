---
title: Video360Player.progressivebitrate
description: Attributo di configurazione per il visualizzatore Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 8%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Attributo di configurazione per il visualizzatore Video360.

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Specifica il bit rate video desiderato (in kilobit al secondo o kbps) da riprodurre da un set video adattivo nel caso in cui il sistema corrente non supporti la riproduzione video adattiva. </p> <p>Il componente raccoglie il flusso video con il bit rate più vicino possibile (ma non superiore) al valore specificato. Se tutti i flussi video del set video adattivo hanno una qualità superiore rispetto al valore specificato, la logica sceglie il bit rate con la qualità più bassa. </p> </td> 
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
