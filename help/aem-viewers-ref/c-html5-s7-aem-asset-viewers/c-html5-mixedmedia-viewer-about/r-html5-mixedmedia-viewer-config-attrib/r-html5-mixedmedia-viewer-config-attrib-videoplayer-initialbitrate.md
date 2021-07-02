---
description: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p>Imposta i bit in bit/bit in bitrate video per secondi o kbps-utilizzati per la riproduzione iniziale del video sui desktop. </p> <p>Se questo valore di bitrate non esiste nel set video adattivo, il lettore video avvia il video con il bitrate più basso successivo. </p> <p>Se è impostato su <span class="codeph"> 0 </span>, il lettore video inizia dal bitrate più basso possibile. Applicabile solo ai sistemi che non dispongono del supporto nativo per video HTML5 HLS (che sono browser Firefox, Chrome e Internet Explorer 11 su Windows 10) e quando la modalità di riproduzione è impostata su <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
