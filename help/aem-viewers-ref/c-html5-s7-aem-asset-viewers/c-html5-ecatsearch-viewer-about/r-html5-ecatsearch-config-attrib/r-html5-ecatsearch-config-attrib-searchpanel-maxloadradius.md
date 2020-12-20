---
description: 'null'
seo-description: 'null'
seo-title: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
topic: Dynamic media
uuid: 37d58c88-3d45-44d9-9f2c-d616d1077906
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---


# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> precaricatore</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica il comportamento di precaricamento del componente. </p> <p>Se impostate su <span class="codeph"> -1</span>, tutte le miniature vengono caricate contemporaneamente quando il componente viene inizializzato o la risorsa cambia. </p> <p> Se impostato su <span class="codeph"> 0</span> vengono caricate solo le miniature visibili. </p> <p>Impostare <span class="codeph"><span class="varname"> preload</span></span> per definire quante righe invisibili vengono precaricate intorno all'area visibile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-4b7952997f9240e581d21bcdb173f9af}

Facoltativo.

## Predefinito {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Esempio {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
