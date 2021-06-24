---
description: FavoritesView.favoritesThumbView
solution: Experience Manager
title: FavoritesView.favoritesThumbView
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Developer,Business Practitioner
exl-id: 3a0a7482-315f-4192-aa6d-e9cc1415194f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---

# FavoritesView.favoritesThumbView{#favoritesview-favoritesthumbview}

[!DNL ` [FavoritesView.|<containerId>_favoritesView.]favoritesThumbArea= *`area`*`]

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

[!DNL `0.1`]

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `favoritesThumbArea=0.5`]
