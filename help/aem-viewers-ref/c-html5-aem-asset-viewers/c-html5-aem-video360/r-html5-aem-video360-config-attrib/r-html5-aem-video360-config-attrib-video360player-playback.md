---
title: Video360Player.playback
description: Attributo di configurazione per il visualizzatore Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
TQID: 'https://experienceleague.adobe.com/2Q41XrgRhpCJXlpHtdIVJkcy2eqVNTK4lSo023yPRoI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 2%

---

# Video360Player.playback{#video-player-playback}

Attributo di configurazione per il visualizzatore Video360.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> automatico|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Imposta il tipo di riproduzione utilizzato dal visualizzatore. </p> <p>Quando è impostato <span class="codeph"> auto</span>, nella maggior parte dei browser desktop e in tutti i dispositivi iOS, il visualizzatore utilizza video streaming HTML5 in formato HLS. Inoltre, si basa sulla riproduzione progressiva di HTML5 su alcuni sistemi come i vecchi Internet Explorer e Android™. </p> <p>Quando è impostato <span class="codeph"> progressive</span>, il visualizzatore si basa solo sulla riproduzione di HTML5 supportata in modalità nativa dai browser e riproduce il video in modo progressivo su tutti i sistemi. </p> <p>Per ulteriori informazioni sulla selezione della riproduzione in modalità nativa <span class="codeph"> auto</span> e <span class="codeph"> progressive</span>, vedere la Guida utente di HTML5 Viewers SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo. Ignorato quando il visualizzatore funziona con un video esterno.

Per informazioni dettagliate, consulta [Supporto video esterno](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760).

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`auto`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
