---
description: Attributo di configurazione per il visualizzatore video interattivo.
seo-description: Attributo di configurazione per il visualizzatore video interattivo.
seo-title: VideoPlayer.play
solution: Experience Manager
title: VideoPlayer.play
topic: Dynamic media
uuid: 2576f433-b9c2-4da1-9a51-f66b71d5df99
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.play{#videoplayer-playback}

Attributo di configurazione per il visualizzatore video interattivo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Imposta il tipo di riproduzione utilizzato dal visualizzatore. </p> <p>Quando <span class="codeph"> è impostata l’opzione Automatico</span> , nella maggior parte dei browser desktop e in tutti i dispositivi iOS il visualizzatore utilizza lo streaming video HTML5 in formato HLS e torna alla riproduzione progressiva HTML5 su alcuni sistemi come Internet Explorer e Android meno recenti. </p> <p>Quando è impostata la modalità <span class="codeph"> progressiva</span> , il visualizzatore utilizza solo la riproduzione HTML5 supportata in modo nativo dai browser e riproduce progressivamente il video su tutti i sistemi. </p> <p>Per ulteriori informazioni sulla selezione della riproduzione nelle modalità native <span class="codeph"> automatica</span> e <span class="codeph"> progressiva</span> , consultate la guida utente dell’SDK per visualizzatori HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`auto`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
