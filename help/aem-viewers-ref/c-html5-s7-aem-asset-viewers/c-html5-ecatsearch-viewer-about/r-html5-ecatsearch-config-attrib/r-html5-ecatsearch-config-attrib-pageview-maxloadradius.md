---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
topic: Dynamic Media
uuid: e60603a5-06dc-43e3-a380-b4d97fc539f1
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

---


# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

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

[!DNL `1`]

## Esempio {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
