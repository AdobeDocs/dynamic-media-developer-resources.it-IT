---
title: FavoritesView.favoritesThumbView
description: FavoritesView.favoritesThumbView
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 5c57fcc8-be67-408a-9c4c-4e15d5fe6410
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# FavoritesView.favoritesThumbView{#favoritesview-favoritesthumbview}

` [FavoritesView.|<containerId>_favoritesView.]favoritesThumbArea= *`area`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> area</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica l'area di ritaglio per la miniatura Preferiti. Espresso come valore relativo alla dimensione totale del fotogramma, con un intervallo da <span class="codeph"> 0</span> a <span class="codeph"> 1,0</span>. </p> <p>Un valore di <span class="codeph"> 1</span> significa che l'intera immagine del fotogramma viene utilizzata per la miniatura. </p> <p>Un valore di <span class="codeph"> 0,1</span> significa che viene utilizzato solo il 10% delle dimensioni del frame. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`0.1`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`favoritesThumbArea=0.5`
