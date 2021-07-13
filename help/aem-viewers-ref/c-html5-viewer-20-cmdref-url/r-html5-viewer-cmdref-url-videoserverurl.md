---
description: Parametro comune a tutti i visualizzatori.
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,Visualizzatori,SDK/API
role: Developer,User
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 5%

---

# videoServerUrl{#videoserverurl}

Parametro comune a tutti i visualizzatori.

>[!NOTE]
>
>Questo comando non si applica al visualizzatore di immagini video.

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Il percorso principale del server video. Se non viene specificato alcun dominio, viene applicato il dominio da cui viene distribuita la pagina. Si applica la risoluzione standard del percorso URI. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-10ee45d637134e0fbcd943c62578cb78}

Facoltativo. Non necessario per il software standard come utilizzo di un servizio.

## Predefinito {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Esempio {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
