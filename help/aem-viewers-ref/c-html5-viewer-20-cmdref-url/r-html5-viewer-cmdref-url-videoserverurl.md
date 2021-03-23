---
description: Parametro comune a tutti i visualizzatori.
seo-description: Parametro comune a tutti i visualizzatori.
seo-title: videoServerUrl
solution: Experience Manager
title: videoServerUrl
uuid: ef9870f9-599b-449d-b713-66abafb80311
feature: Dynamic Media Classic,Visualizzatori,SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '78'
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

