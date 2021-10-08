---
title: Video360Player.playback
description: Attributo di configurazione per il visualizzatore Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Video360Player.playback{#video-player-playback}

Attributo di configurazione per il visualizzatore Video360.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> automatico|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Imposta il tipo di riproduzione utilizzato dal visualizzatore. </p> <p>Quando <span class="codeph"> auto</span> è impostato, nella maggior parte dei browser desktop e in tutti i dispositivi iOS, il visualizzatore utilizza video in streaming HTML5 in formato HLS. Inoltre, torna alla riproduzione progressiva HTML5 su alcuni sistemi come Internet Explorer e Android™. </p> <p>Quando si imposta <span class="codeph"> progressivo</span>, il visualizzatore si basa solo sulla riproduzione HTML5 supportata in modo nativo dai browser e riproduce progressivamente i video su tutti i sistemi. </p> <p>Per ulteriori informazioni sulla selezione della riproduzione nelle modalità native <span class="codeph"> auto</span> e <span class="codeph"> progressive</span>, consulta la Guida utente dell’SDK per visualizzatori HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo. Ignorato quando il visualizzatore funziona con video esterno.

Per ulteriori informazioni, consulta [Supporto video esterno](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) .

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`auto`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
