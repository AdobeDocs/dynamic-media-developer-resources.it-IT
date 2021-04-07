---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Attributo di configurazione per Visualizzatore video interattivo.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Specifica in kbit per secondo (o kbps) il bit rate video desiderato da riprodurre da un set video adattivo nel caso in cui il sistema corrente non supporti la riproduzione video adattiva. </p> <p>Il componente raccoglie il flusso video con il bit rate più vicino possibile (ma non superiore) al valore specificato. Se tutti i flussi video del set video adattivo hanno una qualità superiore rispetto al valore specificato, la logica sceglie il bit rate con la qualità più bassa. </p> </td> 
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
