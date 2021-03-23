---
description: FavoritesView.favoritesThumbView
solution: Experience Manager
title: FavoritesView.favoritesThumbView
uuid: 5c362eb3-dece-4546-8a79-fd79c2852a78
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 6%

---


# FavoritesView.favoritesThumbView{#favoritesview-favoritesthumbview}

` [FavoritesView.|<containerId>_favoritesView.]favoritesThumbArea= *`area`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> area</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica l'area di ritaglio per la miniatura Preferiti. Espresso come valore relativo alla dimensione totale del fotogramma, con un intervallo compreso tra <span class="codeph"> 0</span> e <span class="codeph"> 1.0</span>. </p> <p>Il valore di <span class="codeph"> 1</span> indica che l'intera immagine del fotogramma viene utilizzata per la miniatura. </p> <p>Il valore di <span class="codeph"> 0,1</span> indica che viene utilizzato solo il 10% delle dimensioni del fotogramma. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`0.1`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`favoritesThumbArea=0.5`
