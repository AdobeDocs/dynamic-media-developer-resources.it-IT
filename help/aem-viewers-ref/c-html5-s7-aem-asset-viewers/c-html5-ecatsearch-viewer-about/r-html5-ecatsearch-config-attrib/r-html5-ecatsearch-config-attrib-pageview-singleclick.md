---
description: 'null'
seo-description: 'null'
seo-title: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
topic: Dynamic media
uuid: b08b605e-5ffc-42cc-931d-d67750a8dca8
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di zoom con un solo clic o tocco. Se si imposta su <span class="codeph"> none, </span> lo zoom con un solo clic o un tocco viene disattivato. Se è impostato per <span class="codeph"> lo zoom, facendo </span> clic sull’immagine si esegue lo zoom in un passaggio di zoom; CTRL+clic consente di ridurre un passaggio di zoom. Se si imposta la <span class="codeph"> reimpostazione, </span> si fa clic sull’immagine per ripristinare lo zoom al livello iniziale. Per <span class="codeph"> lo zoomReset </span>, viene applicato il reset se il fattore di zoom corrente è uguale o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-edcfcd6c0bd24ac093442c56450b3c97}

Facoltativo.

## Predefinito {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] su computer desktop; [!DNL `none`] su dispositivi touch.

## Esempio {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]