---
title: VideoPlayer.initialbitrate
description: VideoPlayer.initialbitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
TQID: 'https://experienceleague.adobe.com/43fGvsD0G1miDbzE8EQnXmTVrlCQEOP9V2r0ji83yww'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`valore`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> valore </span> </span> </p> </td> 
   <td colname="col2"> <p>Imposta il bitrate video (in kilobit al secondo o Kbps) utilizzato per la riproduzione iniziale del video sui desktop. </p> <p>Se questo valore di bitrate non esiste nel set di video adattivi, il lettore video avvia il video che ha il bitrate inferiore più prossimo. </p> <p>Se è impostato su <span class="codeph"> 0 </span>, il lettore video inizia dal bitrate più basso possibile. Applicabile solo per i sistemi che non dispongono del supporto nativo per HTML5 HLS video (che sono browser Firefox, Chrome e Internet Explorer 11 su Windows 10) e quando la modalità di riproduzione è impostata su <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
