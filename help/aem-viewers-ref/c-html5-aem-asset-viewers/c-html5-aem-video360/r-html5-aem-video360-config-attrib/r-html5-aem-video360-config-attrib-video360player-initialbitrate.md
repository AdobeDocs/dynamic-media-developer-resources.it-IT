---
description: Attributo di configurazione per il visualizzatore Video360.
seo-description: Attributo di configurazione per il visualizzatore Video360.
seo-title: Video360Player.initialbitrate
solution: Experience Manager
title: Video360Player.initialbitrate
topic: Dynamic media
uuid: a23fa941-6dd2-41c0-aca9-06f0cdb027b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 8%

---


# Video360Player.initialbitrate{#video-player-initialbitrate}

Attributo di configurazione per il visualizzatore Video360.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Imposta il bitrate video (in kbit al secondo o kbps) utilizzato per la riproduzione iniziale del video su un desktop. </p> <p>Se questo valore di bitrate non esiste nel set video adattivo, il lettore video inizia con il video con bitrate successivo inferiore. </p> <p>Se è impostato su <span class="codeph"> 0</span>, il lettore video inizia dal bitrate più basso possibile. </p> <p>Applicabile solo ai sistemi che non dispongono del supporto nativo per video HTML5 HLS (come i browser Firefox, Chrome e Internet Explorer 11 in Windows 10) e quando la modalità di riproduzione è impostata su auto. </p> </td> 
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

