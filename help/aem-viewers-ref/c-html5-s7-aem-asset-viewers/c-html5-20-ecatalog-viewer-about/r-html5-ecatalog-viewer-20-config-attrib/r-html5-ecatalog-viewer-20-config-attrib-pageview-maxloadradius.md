---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
topic: Dynamic media
uuid: 425624c5-3cbe-4b63-8c6b-eff31f2ed919
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

---


# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> precaricatore</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica il comportamento di precaricamento del componente. </p> <p>Se è impostata su <span class="codeph"> -1</span>, il componente precarica tutti i fotogrammi del catalogo quando è in stato di inattività. </p> <p> Se impostato su <span class="codeph"> 0</span>, il componente carica solo il fotogramma attualmente visibile, precedente e successivo. </p> <p>Impostate <span class="codeph"><span class="varname"> precaricatore</span></span> per definire quanti fotogrammi invisibili intorno al fotogramma attualmente visualizzato vengono precaricati in stato di inattività. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-4b7952997f9240e581d21bcdb173f9af}

Facoltativo.

## Predefinito {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## Esempio {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
