---
description: Indica se il visualizzatore inizia a caricare il contenuto video prima dell’avvio della riproduzione.
seo-description: Indica se il visualizzatore inizia a caricare il contenuto video prima dell’avvio della riproduzione.
seo-title: Video360Player.preload
solution: Experience Manager
title: Video360Player.preload
uuid: 6e3b95b8-d585-4164-8665-6211000689fe
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video VR 360
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

---


# Video360Player.preload{#video-player-preload}

Indica se il visualizzatore inizia a caricare il contenuto video prima dell’avvio della riproduzione.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

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
