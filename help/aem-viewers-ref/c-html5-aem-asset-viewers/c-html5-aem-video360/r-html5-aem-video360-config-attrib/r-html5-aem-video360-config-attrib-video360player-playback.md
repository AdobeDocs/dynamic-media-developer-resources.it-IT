---
description: Attributo di configurazione per il visualizzatore Video360.
seo-description: Attributo di configurazione per il visualizzatore Video360.
seo-title: Video360Player.playback
solution: Experience Manager
title: Video360Player.playback
topic: Dynamic media
uuid: ce814963-5cb8-408e-9d57-e7b7e61e0fab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.playback{#video-player-playback}

Attributo di configurazione per il visualizzatore Video360.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Imposta il tipo di riproduzione utilizzato dal visualizzatore. </p> <p>Quando <span class="codeph"> è impostata l’opzione Automatico</span> , nella maggior parte dei browser desktop e in tutti i dispositivi iOS il visualizzatore utilizza lo streaming video HTML5 in formato HLS e torna alla riproduzione progressiva HTML5 su alcuni sistemi come Internet Explorer e Android meno recenti. </p> <p>Quando è impostata la modalità <span class="codeph"> progressiva</span> , il visualizzatore utilizza solo la riproduzione HTML5 supportata in modo nativo dai browser e riproduce progressivamente il video su tutti i sistemi. </p> <p>Per ulteriori informazioni sulla selezione della riproduzione nelle modalità native <span class="codeph"> automatica</span> e <span class="codeph"> progressiva</span> , consultate la guida utente dell’SDK per visualizzatori HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo. Ignorato quando il visualizzatore funziona con video esterno.

Per informazioni dettagliate, consultate Supporto [video](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) esterno.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`auto`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
