---
description: Attributo di configurazione per il visualizzatore Video360.
solution: Experience Manager
title: Video360Player.playback
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video VR 360
role: Developer,Business Practitioner
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 6%

---

# Video360Player.playback{#video-player-playback}

Attributo di configurazione per il visualizzatore Video360.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> automatico|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Imposta il tipo di riproduzione utilizzato dal visualizzatore. </p> <p>Quando <span class="codeph"> auto</span> è impostato, nella maggior parte dei browser desktop e in tutti i dispositivi iOS il visualizzatore utilizza video in streaming HTML5 in formato HLS, e torna alla riproduzione progressiva HTML5 su alcuni sistemi come i vecchi Internet Explorer e Android. </p> <p>Quando si imposta <span class="codeph"> progressivo</span>, il visualizzatore si basa solo sulla riproduzione HTML5 supportata in modo nativo dai browser e riproduce progressivamente i video su tutti i sistemi. </p> <p>Per ulteriori informazioni sulla selezione della riproduzione nelle modalità native dei visualizzatori HTML5, vedere la Guida utente dell'SDK per visualizzatori HTML5.<span class="codeph"></span><span class="codeph"></span> </p> </td> 
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
