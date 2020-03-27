---
description: 'null'
seo-description: 'null'
seo-title: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
topic: Dynamic media
uuid: c62302b0-d034-49d4-b5a8-1a77a46fe889
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di zoom con doppio clic o tocco. Se si imposta su <span class="codeph"> none, lo zoom con doppio clic o con il tocco </span> viene disattivato. Se è impostato per <span class="codeph"> lo zoom, facendo </span> clic sull’immagine si esegue lo zoom in un passaggio di zoom; CTRL+clic consente di ridurre un passaggio di zoom. Se si imposta la <span class="codeph"> reimpostazione, </span> si fa clic sull’immagine per ripristinare lo zoom al livello iniziale. Per <span class="codeph"> lo zoomReset </span>, viene applicato il reset se il fattore di zoom corrente è uguale o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Facoltativo.

## Predefinito {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] su computer desktop; [!DNL `zoomReset`] su dispositivi touch.

## Esempio {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
