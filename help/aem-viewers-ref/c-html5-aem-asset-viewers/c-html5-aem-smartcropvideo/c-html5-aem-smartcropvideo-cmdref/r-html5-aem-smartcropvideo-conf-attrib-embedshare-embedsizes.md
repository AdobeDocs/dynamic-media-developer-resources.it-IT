---
title: EmbedShare.embedsizes
description: Attributo di configurazione per Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 11%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Attributo di configurazione per Smart Crop Video Viewer.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`larghezza`*, *`altezza`*[,0|1][; *`larghezza`*, *`altezza`*[,0|1]]`

Specifica un elenco di dimensioni da incorporare per la casella combinata dimensioni nella finestra di dialogo modale di condivisione da incorporare.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> Larghezza da incorporare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>Altezza da incorporare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica se la voce dell'elenco deve essere inizialmente preselezionata nella casella combinata. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
