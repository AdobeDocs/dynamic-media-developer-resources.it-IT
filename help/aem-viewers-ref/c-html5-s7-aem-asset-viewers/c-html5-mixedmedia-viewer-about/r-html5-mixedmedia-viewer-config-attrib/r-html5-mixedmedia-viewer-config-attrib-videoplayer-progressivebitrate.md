---
description: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 4%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica (in kbit per secondo o kbps) il bit rate video desiderato da riprodurre da un set video adattivo nel caso in cui il sistema corrente non supporti la riproduzione video adattiva. </p> <p>Il componente raccoglie il flusso video con il bitrate più vicino possibile (ma non superiore) al valore specificato. Se tutti i flussi video nel set video adattivo hanno una qualità superiore rispetto al valore specificato, la logica sceglie il bitrate con la qualità più bassa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
