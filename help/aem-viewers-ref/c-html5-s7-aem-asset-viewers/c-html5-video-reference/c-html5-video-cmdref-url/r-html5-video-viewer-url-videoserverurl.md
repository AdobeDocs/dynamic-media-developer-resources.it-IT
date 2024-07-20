---
title: videoServerUrl
description: Comando URL per Visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 945c32e0-a67b-4c27-b661-26510615d757
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 3%

---

# videoServerUrl{#videoserverurl}

Comando URL per Visualizzatore video.

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Percorso root del server video. Se non viene specificato alcun dominio, viene applicato il dominio da cui è trasmessa la pagina. È applicabile la risoluzione del percorso URI standard. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo. Non necessario per l’utilizzo SaaS standard.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
