---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Developer,Business Practitioner
exl-id: acbcea10-950d-4f98-be5a-5aead9f4e0d9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

[!DNL `[ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> precaricare</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica il comportamento di precaricamento del componente. </p> <p>Se è impostato su <span class="codeph"> -1</span>, le miniature vengono caricate simultaneamente quando il componente viene inizializzato o la risorsa cambia. </p> <p>Se è impostato su <span class="codeph"> 0</span> vengono caricate solo le miniature visibili. </p> <p>Imposta <span class="codeph"><span class="varname"> preload</span></span> definisce quante righe/colonne invisibili intorno all'area visibile vengono precaricate. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-a3abd04c03e14c238a07349ce50d8310}

Facoltativo.

## Predefinito {#section-c60e81667965460cbf03378a1ab9b187}

[!DNL `1`]

## Esempio {#section-472614b59e04430490a7f16c932bce89}

[!DNL `maxloadradius=0`]
