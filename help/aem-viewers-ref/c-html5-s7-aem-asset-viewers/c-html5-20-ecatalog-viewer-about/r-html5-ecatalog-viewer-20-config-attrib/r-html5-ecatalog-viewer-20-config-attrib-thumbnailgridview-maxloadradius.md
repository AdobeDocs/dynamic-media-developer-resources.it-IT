---
title: ThumbnailGridView.maxloadradius
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e93de3b5-b42d-4db8-90b9-9e2aa53af775
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 5%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica il comportamento di precaricamento del componente. </p> <p>Se è impostato su <span class="codeph"> -1</span>, le miniature vengono caricate contemporaneamente quando il componente viene inizializzato o la risorsa cambia. </p> <p>Se è impostato su <span class="codeph"> 0</span>, vengono caricate solo le miniature visibili. </p> <p>Il set <span class="codeph"><span class="varname"> preloadnbr</span></span> definisce quante righe/colonne invisibili vengono precaricate attorno all'area visibile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-a3abd04c03e14c238a07349ce50d8310}

Facoltativo.

## Predefinito {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## Esempio {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`
