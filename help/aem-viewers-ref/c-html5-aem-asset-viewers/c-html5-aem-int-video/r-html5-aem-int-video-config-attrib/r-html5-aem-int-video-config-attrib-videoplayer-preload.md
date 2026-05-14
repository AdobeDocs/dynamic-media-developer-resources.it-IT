---
title: VideoPlayer.preload
description: Indica se il visualizzatore inizia a caricare il contenuto video prima dell’inizio della riproduzione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: afabbfde-e003-4fee-a4ef-0fc4c43fd960
TQID: 'https://experienceleague.adobe.com/T-tJLZX4XCIAQ6NjwNVYrbuM1czp25M6vAB0WVOZ1No'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

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
