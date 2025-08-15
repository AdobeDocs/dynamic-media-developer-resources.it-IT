---
title: VideoPlayer.mutevolume
description: Attributo di configurazione per Video visualizzatore.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 8f644a40-7fd9-4edd-be29-698635b46507
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 5%

---

# VideoPlayer.mutevolume{#videoplayer-mutevolume}

Attributo di configurazione per Video visualizzatore.

`[VideoPlayer.|<containerId>_videoPlayer.]mutevolume=0|1`

<table id="table_2A4F898BBF88417DB0834B7F78637F5D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Imposta la modalità disattivata per la riproduzione video durante il caricamento iniziale. Se impostato su <span class="codeph"> 1 </span> , l'audio del volume viene disattivato; in caso contrario, il video viene riprodotto con l'audio. Su alcuni dispositivi, l'audio della riproduzione video durante il caricamento consente anche la riproduzione automatica del video. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`mutevolume=1`
