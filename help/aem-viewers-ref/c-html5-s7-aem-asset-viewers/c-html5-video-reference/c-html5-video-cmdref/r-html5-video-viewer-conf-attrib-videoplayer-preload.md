---
description: Indica se il visualizzatore inizia a caricare il contenuto video prima dell’avvio della riproduzione.
solution: Experience Manager
title: VideoPlayer.preload
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video
role: Developer,User
exl-id: cee887f6-bbd9-46dd-aa41-03493596fcf4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# VideoPlayer.preload{#videoplayer-preload}

Indica se il visualizzatore inizia a caricare il contenuto video prima dell’avvio della riproduzione.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Se è impostato su <span class="codeph"> 1 </span> il video inizia a essere scaricato subito dopo l’impostazione della risorsa; in caso contrario, il precaricamento viene avviato solo dopo che l’utente finale o una chiamata API ha avviato la riproduzione. </p> <p>Se impostato su <span class="codeph"> 0 </span>, alcune funzioni potrebbero non funzionare fino all'avvio della riproduzione; in particolare, l'operazione di ricerca non aggiornerà il fotogramma video. Se l’immagine poster è disabilitata, il visualizzatore viene visualizzato come un’area vuota invece del primo fotogramma video. </p> <p>La disattivazione del precaricamento video potrebbe essere ignorata in alcune versioni dei browser Internet Explorer 11 e Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
