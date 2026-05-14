---
title: PageView.singleclick
description: PageView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
TQID: 'https://experienceleague.adobe.com/UKTYi08iCk95i-eUL1YYLZEQnMtNu3u2-tbs0NTBbj4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di clic/tocco per eseguire lo zoom. L'impostazione su <span class="codeph"> none </span> disattiva lo zoom con clic/tocco. Se è impostato su <span class="codeph">, lo zoom di </span> facendo clic sull'immagine si ingrandisce di un livello; se si fa clic tenendo premuto CTRL l'immagine si riduce di un livello. L'impostazione su <span class="codeph"> per il ripristino di </span> fa sì che un singolo clic sull'immagine ripristini il livello di zoom iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il ripristino se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-edcfcd6c0bd24ac093442c56450b3c97}

Facoltativo.

## Predefinito {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` nei computer desktop; `none` nei dispositivi touch.

## Esempio {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
