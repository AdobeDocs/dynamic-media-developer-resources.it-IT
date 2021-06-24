---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Developer,Business Practitioner
exl-id: e6baef83-b4a8-4bef-bb13-263f3875030d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di doppio clic/tocco per lo zoom. Impostando su <span class="codeph"> none </span> si disattiva lo zoom con doppio clic o tocco. Se è impostato su <span class="codeph"> zoom </span> facendo clic sull'immagine si ingrandisce un solo passaggio di zoom; CTRL+clic consente di ingrandire un passaggio di zoom. Se si imposta il valore <span class="codeph"> reset </span> , si farà clic sull'immagine per ripristinare lo zoom al livello iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il reset se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Facoltativo.

## Predefinito {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] su computer desktop;  [!DNL `zoomReset`] su dispositivi touch.

## Esempio {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
