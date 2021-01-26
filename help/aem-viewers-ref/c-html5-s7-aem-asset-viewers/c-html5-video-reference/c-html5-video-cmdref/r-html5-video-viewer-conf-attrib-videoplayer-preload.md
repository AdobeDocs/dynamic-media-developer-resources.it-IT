---
description: Indica se il visualizzatore avvia il caricamento del contenuto video prima dell'avvio della riproduzione.
seo-description: Indica se il visualizzatore avvia il caricamento del contenuto video prima dell'avvio della riproduzione.
seo-title: VideoPlayer.preload
solution: Experience Manager
title: VideoPlayer.preload
topic: Dynamic Media
uuid: 2aaae96d-d42d-4984-aec9-86e06b3c711c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# VideoPlayer.preload{#videoplayer-preload}

Indica se il visualizzatore avvia il caricamento del contenuto video prima dell&#39;avvio della riproduzione.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Se è impostato su <span class="codeph"> 1 </span> il video inizia a essere scaricato subito dopo che la risorsa è stata impostata; in caso contrario, il precaricamento viene avviato solo dopo che l’utente finale o una chiamata API ha avviato la riproduzione. </p> <p>Se impostata su <span class="codeph"> 0 </span>, alcune funzioni potrebbero non funzionare fino all'avvio della riproduzione; in particolare, l’operazione di ricerca non aggiornerà il fotogramma video. Se l’immagine poster è disattivata, il visualizzatore viene visualizzato come un’area vuota invece del primo fotogramma video. </p> <p>La disattivazione del precaricamento video potrebbe essere ignorata in alcune versioni dei browser Internet Explorer 11 ed Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
