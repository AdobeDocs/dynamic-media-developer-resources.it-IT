---
title: VideoPlayer.playback
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
TQID: 'https://experienceleague.adobe.com/VnLfO1MI9EIpeoP4fpwMufyy-J2g615LOosZ4hLZlt8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

Attributo di configurazione per Visualizzatore video interattivo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> automatico|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Imposta il tipo di riproduzione utilizzato dal visualizzatore. </p> <p>Quando è impostato <span class="codeph"> auto</span>, nella maggior parte dei browser desktop e in tutti i dispositivi iOS, il visualizzatore utilizza video streaming HTML5 in formato HLS. Inoltre, si basa sulla riproduzione progressiva di HTML5 su alcuni sistemi come i vecchi Internet Explorer e Android™. </p> <p>Quando è impostato <span class="codeph"> progressive</span>, il visualizzatore si basa solo sulla riproduzione di HTML5 supportata in modalità nativa dai browser e riproduce il video in modo progressivo su tutti i sistemi. </p> <p>Per ulteriori informazioni sulla selezione della riproduzione in modalità nativa <span class="codeph"> auto</span> e <span class="codeph"> progressive</span>, vedere la Guida utente di HTML5 Viewers SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`auto`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
