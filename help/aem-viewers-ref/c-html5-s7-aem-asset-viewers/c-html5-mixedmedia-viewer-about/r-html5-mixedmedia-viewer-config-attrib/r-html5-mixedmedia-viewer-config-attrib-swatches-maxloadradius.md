---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
uuid: eb4a6fca-da18-4291-b7fb-e402156c85a0
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

---


# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_012E1D178BFA4BD9814A7AAD2B4403BB"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> precaricare</span></span> </p> </td> 
   <td> <p>Specifica il comportamento di precaricamento del componente. Quando è impostato su <span class="codeph"> -1</span> tutti i campioni vengono caricati contemporaneamente quando il componente viene inizializzato o la risorsa viene modificata. </p> <p>Se è impostato su <span class="codeph"> 0</span> vengono caricati solo i campioni visibili. </p> <p><span class="codeph"><span class="varname"> </span></span> precaricare definisce quante righe/colonne invisibili vengono precaricate intorno all’area visibile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=-1`
