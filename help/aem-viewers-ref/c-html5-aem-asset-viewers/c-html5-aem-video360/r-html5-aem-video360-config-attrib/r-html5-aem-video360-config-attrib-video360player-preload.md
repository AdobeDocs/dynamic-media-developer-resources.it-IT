---
title: Video360Player.preload
description: Indica se il visualizzatore inizia a caricare il contenuto video prima dell’avvio della riproduzione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Video360Player.preload{#video-player-preload}

Indica se il visualizzatore inizia a caricare il contenuto video prima dell’avvio della riproduzione.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Se è impostato su <span class="codeph"> 1 </span>, il video inizia a essere scaricato subito dopo l’impostazione della risorsa. In caso contrario, il precaricamento viene avviato solo dopo che l’utente finale o una chiamata API ha avviato la riproduzione. </p> <p>Se è impostato su <span class="codeph"> 0 </span>, alcune funzioni potrebbero non funzionare fino all'avvio della riproduzione. Nello specifico, l'operazione di ricerca non aggiorna il fotogramma video. Se l’immagine poster è disabilitata, il visualizzatore viene visualizzato come un’area vuota invece del primo fotogramma video. </p> <p>La disattivazione del precaricamento video può essere ignorata in alcune versioni dei browser Internet Explorer 11 e Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
