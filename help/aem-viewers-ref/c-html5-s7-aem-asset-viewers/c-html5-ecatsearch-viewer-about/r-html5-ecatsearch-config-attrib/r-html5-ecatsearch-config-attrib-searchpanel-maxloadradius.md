---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---


# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> precaricare</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica il comportamento di precaricamento del componente. </p> <p>Se è impostato su <span class="codeph"> -1</span>, tutte le miniature vengono caricate simultaneamente quando il componente viene inizializzato o la risorsa cambia. </p> <p> Se impostato su <span class="codeph"> 0</span> vengono caricate solo le miniature visibili. </p> <p>Imposta <span class="codeph"><span class="varname"> preload</span></span> per definire quante righe invisibili vengono precaricate intorno all'area visibile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-4b7952997f9240e581d21bcdb173f9af}

Facoltativo.

## Predefinito {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Esempio {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
