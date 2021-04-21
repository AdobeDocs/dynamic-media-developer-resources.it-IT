---
description: Attributo di configurazione per il visualizzatore video per file multimediali diversi.
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

Attributo di configurazione per il visualizzatore video per file multimediali diversi.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> automatico|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Imposta il tipo di riproduzione utilizzato dal visualizzatore. Quando <span class="codeph"> auto</span> è impostato, nella maggior parte dei browser desktop e in tutti i dispositivi iOS, il visualizzatore utilizza video in streaming HTML5 in formato HLS. Ritorna alla riproduzione progressiva HTML5 su alcuni sistemi come Internet Explorer e Android. </p> <p>Se è specificato <span class="codeph"> progressivo</span>, il visualizzatore si basa solo sulla riproduzione HTML5 supportata in modo nativo dai browser e riproduce progressivamente i video su tutti i sistemi. </p> <p>Per ulteriori informazioni sulla selezione della riproduzione nelle modalità automatica e progressiva, consulta la Guida utente dell’SDK per visualizzatori. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
