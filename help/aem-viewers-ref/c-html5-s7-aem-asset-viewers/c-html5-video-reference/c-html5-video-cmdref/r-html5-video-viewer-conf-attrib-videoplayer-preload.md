---
title: VideoPlayer.preload
description: Indica se il visualizzatore inizia a caricare il contenuto video prima dell’inizio della riproduzione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: cee887f6-bbd9-46dd-aa41-03493596fcf4
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# VideoPlayer.preload{#videoplayer-preload}

Indica se il visualizzatore inizia a caricare il contenuto video prima dell’inizio della riproduzione.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Se è impostato su <span class="codeph"> 1 </span>, il download del video inizia subito dopo l'impostazione della risorsa; in caso contrario, il precaricamento inizia solo dopo che la riproduzione è stata avviata dall'utente finale o da una chiamata API. </p> <p>Se è impostato su <span class="codeph"> 0 </span>, alcune funzionalità potrebbero non funzionare fino all'avvio della riproduzione; in particolare, l'operazione di ricerca non aggiorna il fotogramma video. Se l'immagine del poster è disattivata, il visualizzatore viene visualizzato come un'area vuota invece del primo fotogramma video. </p> <p>La disattivazione del precaricamento video potrebbe essere ignorata in alcune versioni di Internet Explorer 11 e dei browser Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
