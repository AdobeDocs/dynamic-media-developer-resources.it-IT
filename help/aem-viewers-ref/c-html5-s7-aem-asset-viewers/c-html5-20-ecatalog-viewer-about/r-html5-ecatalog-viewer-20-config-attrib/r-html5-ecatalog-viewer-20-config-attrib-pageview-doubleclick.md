---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
topic: Dynamic media
uuid: ac4fb532-f554-4831-b341-7f8d6ef3a1c0
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di zoom con doppio clic o tocco. Se si imposta su <span class="codeph"> none </span>, lo zoom con doppio clic/tocco viene disattivato. Se è impostato su <span class="codeph"> zoom </span>, facendo clic sull'immagine si esegue lo zoom in un passaggio di zoom; CTRL+clic consente di ridurre un passaggio di zoom. Se si imposta <span class="codeph"> reimposta </span>, lo zoom viene reimpostato al livello iniziale con un solo clic sull'immagine. Per <span class="codeph"> zoomReset </span>, viene applicato reset se il fattore di zoom corrente è uguale o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Facoltativo.

## Predefinito {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` su computer desktop;  `zoomReset` su dispositivi touch.

## Esempio {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
