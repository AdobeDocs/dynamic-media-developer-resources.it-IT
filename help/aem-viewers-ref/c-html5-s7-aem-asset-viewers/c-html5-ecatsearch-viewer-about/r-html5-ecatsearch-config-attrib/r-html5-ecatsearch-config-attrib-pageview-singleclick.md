---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffe77be7-bf12-4e9d-9355-2857d366d14e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di clic/tocco per eseguire lo zoom. Impostazione di <span class="codeph"> nessuno </span> disattiva lo zoom con clic/tocco singolo. Se impostato su <span class="codeph"> zoom </span> se si fa clic sull'immagine, questa si ingrandisce di un livello; se si fa clic tenendo premuto CTRL l'immagine si riduce di un livello. Impostazione di <span class="codeph"> ripristina </span> fa in modo che, con un singolo clic, l'immagine ripristini il livello di zoom iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il ripristino se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-edcfcd6c0bd24ac093442c56450b3c97}

Facoltativo.

## Predefinito {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] su computer desktop; [!DNL `none`] sui dispositivi touch.

## Esempio {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]
