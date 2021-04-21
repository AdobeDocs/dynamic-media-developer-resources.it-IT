---
description: FavoritesView.maxloadradius
solution: Experience Manager
title: FavoritesView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 5%

---


# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il comportamento di precaricamento del componente. </p> <p>Se è impostato su <span class="codeph"> -1</span>, tutte le miniature vengono caricate simultaneamente quando il componente viene inizializzato o la risorsa viene modificata. </p> <p>Se è impostato su <span class="codeph"> 0</span>, vengono caricate solo le miniature visibili. </p> <p> Se è impostato su <span class="codeph"><span class="varname"> preload</span></span>, è possibile specificare quante righe invisibili intorno all'area visibile vengono precaricate. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `1`]

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `maxloadradius=0`]
