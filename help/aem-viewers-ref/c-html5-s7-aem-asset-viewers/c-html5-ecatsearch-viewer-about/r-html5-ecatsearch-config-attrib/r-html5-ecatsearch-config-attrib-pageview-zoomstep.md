---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d92e56ae-2bb6-46f6-b0f7-64b867492a37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 3%

---

# PageView.zoomstep{#pageview-zoomstep}

[!DNL `[PageView.|<containerId>_pageView.]zoomstep= *`passaggio`*[, *`limit`*]`]

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> passaggio</span></span> </p> </td> 
   <td colname="col2"> <p> Configura il numero di azioni di zoom in/zoom out necessarie per aumentare/ridurre la risoluzione di un fattore di 2. La modifica della risoluzione per ogni azione di zoom è 2^1 per incremento. Imposta su <span class="codeph"> 0</span> per effettuare lo zoom a risoluzione massima con una singola azione di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limit</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica la risoluzione di zoom massima, relativa alla risoluzione massima dell'immagine. Il valore predefinito è <span class="codeph"> 1,0</span>, che non consente lo zoom oltre la risoluzione massima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-636d35a4791447039f1902973f568320}

Facoltativo.

## Predefinito {#section-ad8a5fe2383e4c228bf177a41b53d921}

[!DNL `1,1`]

## Esempio {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]
