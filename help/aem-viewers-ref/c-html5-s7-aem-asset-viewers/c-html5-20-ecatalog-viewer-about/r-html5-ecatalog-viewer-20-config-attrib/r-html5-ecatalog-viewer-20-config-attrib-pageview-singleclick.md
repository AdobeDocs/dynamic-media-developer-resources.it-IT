---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,User
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di tocco/clic singolo per lo zoom. Impostando su <span class="codeph"> none </span> si disattiva lo zoom con un solo clic o tocco. Se è impostato su <span class="codeph"> zoom </span> facendo clic sull'immagine si ingrandisce un solo passaggio di zoom; CTRL+clic consente di ingrandire un passaggio di zoom. Se si imposta il valore <span class="codeph"> reset </span> , si farà clic sull'immagine per ripristinare lo zoom al livello iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il reset se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-edcfcd6c0bd24ac093442c56450b3c97}

Facoltativo.

## Predefinito {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` su computer desktop;  `none` su dispositivi touch.

## Esempio {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
