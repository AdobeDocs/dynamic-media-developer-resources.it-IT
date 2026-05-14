---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5d978d21-7942-4bd6-b742-9bf4b6fd3ebe
TQID: 'https://experienceleague.adobe.com/DLfxxr5GFbVXJIny4baU6QSFtkEU3OAMc48Em1B6REs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 3%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`passaggio`*[, *`limite`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> passaggio</span></span> </p> </td> 
   <td colname="col2"> <p> Configura il numero di azioni di zoom in/zoom out necessarie per aumentare/ridurre la risoluzione di un fattore di 2. La modifica della risoluzione per ogni azione di zoom è 2^1 per incremento. Imposta su <span class="codeph"> 0</span> per effettuare lo zoom a risoluzione massima con una singola azione di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Limite <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> Specifica la risoluzione di zoom massima, relativa alla risoluzione massima dell'immagine. Il valore predefinito è <span class="codeph"> 1.0</span>, che non consente lo zoom oltre la risoluzione massima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
