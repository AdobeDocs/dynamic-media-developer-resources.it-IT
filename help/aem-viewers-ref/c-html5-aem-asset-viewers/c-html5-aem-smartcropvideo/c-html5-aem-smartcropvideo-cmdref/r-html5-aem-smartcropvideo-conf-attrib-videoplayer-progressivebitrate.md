---
title: SmartCropVideoPlayer.progressivebitrate
description: Attributo di configurazione per il visualizzatore video Ritaglio avanzato.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 25e3e7e9-0979-472c-a589-aaf0e221b885
TQID: 'https://experienceleague.adobe.com/HSShyhUx64vEYIAuInb1sRH5UAdknbAkQWFjYv4yvxo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 3%

---

# SmartCropVideoPlayer.progressivebitrate{#smartcropvideoplayer-progressivebitrate}

Attributo di configurazione per il visualizzatore video Ritaglio avanzato.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]progressivebitrate= *`valore`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Valore <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p> Specifica il bitrate video desiderato, in kilobit al secondo o Kbps, per la riproduzione da un set video adattivo nel caso in cui il sistema corrente non supporti la riproduzione di video adattativi. </p> <p>Il componente raccoglie il flusso video con il bitrate più simile (ma non superiore) possibile al valore specificato. Se tutti i flussi video nel set di video adattivi hanno una qualità superiore rispetto al valore specificato, la logica sceglie il bitrate con la qualità più bassa. </p> </td> 
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
