---
description: Stringa di comando Image Server applicata a tutte le miniature.
solution: Experience Manager
title: FavoritesView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 114cc5b7-32b9-4d16-ab93-a66f3ec666e0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

---

# FavoritesView.iscommand{#favoritesview-iscommand}

Stringa di comando Image Server applicata a tutte le miniature.

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Se specificato nell’URL, tutte le occorrenze di <span class="codeph"> E</span> e <span class="codeph"> =</span> deve essere codificato HTTP come <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>, rispettivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

Nessuno.

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Se specificato nell’URL del visualizzatore.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

Se specificato nei dati di configurazione.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
