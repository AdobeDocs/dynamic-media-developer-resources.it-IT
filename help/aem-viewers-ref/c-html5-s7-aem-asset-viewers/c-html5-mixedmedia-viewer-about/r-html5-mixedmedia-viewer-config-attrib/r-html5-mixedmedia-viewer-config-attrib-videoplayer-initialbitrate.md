---
description: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: 11426516-8336-4186-84b4-15ce5ec7e764
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p>Imposta il bitrate video in kbit per secondi o kbps, utilizzato per la riproduzione iniziale del video su computer desktop. </p> <p>Se questo valore di bitrate non esiste nel set video adattivo, il lettore video avvia il video con il bitrate più basso successivo. </p> <p>Se è impostato su <span class="codeph"> 0 </span>, il lettore video inizia dal bitrate più basso possibile. Applicabile solo ai sistemi che non dispongono del supporto nativo per video HTML5 HLS (che sono browser Firefox, Chrome e Internet Explorer 11 in Windows 10) e quando la modalità di riproduzione è impostata su <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
