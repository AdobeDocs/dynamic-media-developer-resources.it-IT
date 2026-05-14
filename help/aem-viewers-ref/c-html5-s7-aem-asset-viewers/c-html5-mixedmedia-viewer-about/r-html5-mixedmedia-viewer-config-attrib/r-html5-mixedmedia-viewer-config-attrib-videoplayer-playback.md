---
title: VideoPlayer.playback
description: Attributo di configurazione per visualizzatore video per file multimediali diversi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
TQID: 'https://experienceleague.adobe.com/BWApI4QtEvmeQk1vNJDLtKIvrG3uO02oUlOVEGhyl2s'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

Attributo di configurazione per visualizzatore video per file multimediali diversi.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> automatico|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Imposta il tipo di riproduzione utilizzato dal visualizzatore. Quando è impostato <span class="codeph"> auto</span>, nella maggior parte dei browser desktop e in tutti i dispositivi iOS, il visualizzatore utilizza video streaming HTML5 in formato HLS. Si basa sulla riproduzione progressiva di HTML5 su alcuni sistemi come i vecchi Internet Explorer e Android™. </p> <p>Se si specifica <span class="codeph"> progressive</span>, il visualizzatore si basa solo sulla riproduzione di HTML5 supportata in modalità nativa dai browser e riproduce il video in modo progressivo su tutti i sistemi. </p> <p>Per ulteriori informazioni sulla selezione della riproduzione in modalità automatica e progressiva, consultare la Guida utente di Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
