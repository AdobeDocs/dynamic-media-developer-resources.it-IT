---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e6baef83-b4a8-4bef-bb13-263f3875030d
TQID: 'https://experienceleague.adobe.com/TezA2ok7gtbTfgitLMsY4e3FF2pHsEGw-rmABoYCPPA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di doppio clic/tocco per eseguire lo zoom. L'impostazione su <span class="codeph"> none </span> disabilita lo zoom con doppio clic/tocco. Se è impostato su <span class="codeph">, lo zoom di </span> facendo clic sull'immagine si ingrandisce di un livello; se si fa clic tenendo premuto CTRL l'immagine si riduce di un livello. L'impostazione su <span class="codeph"> per il ripristino di </span> fa sì che un singolo clic sull'immagine ripristini il livello di zoom iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il ripristino se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Facoltativo.

## Predefinito {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] nei computer desktop; [!DNL `zoomReset`] nei dispositivi touch.

## Esempio {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
