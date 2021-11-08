---
title: SmartCropVideoPlayer.preload
description: Indica se il visualizzatore inizia a caricare il contenuto video prima dell’avvio della riproduzione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

Indica se il visualizzatore inizia a caricare il contenuto video prima dell’avvio della riproduzione.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Se impostato su <span class="codeph"> 1 </span> il video inizia a essere scaricato subito dopo l’impostazione della risorsa; in caso contrario, il precaricamento viene avviato solo dopo che l’utente finale o una chiamata API ha avviato la riproduzione. </p> <p>Se impostato su <span class="codeph"> 0 </span> alcune funzioni potrebbero non funzionare finché la riproduzione non riprende; in particolare, l'operazione di ricerca non aggiorna il fotogramma video. Se l’immagine poster è disabilitata, il visualizzatore viene visualizzato come un’area vuota invece del primo fotogramma video. </p> <p>La disattivazione del precaricamento video può essere ignorata in alcune versioni dei browser Internet Explorer 11 e Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
