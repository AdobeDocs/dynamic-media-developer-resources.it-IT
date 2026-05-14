---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
TQID: 'https://experienceleague.adobe.com/utzPqD5UMx7TnJK8FvqflzoSjOWGVaGXhKlviY1U9xQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`larghezza`*[; *`larghezza`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Configura il modo in cui il componente recupera le nuove immagini per la visualizzazione principale e a comparsa durante il ridimensionamento. </p> <p>Impostato su <span class="codeph"> 0 </span>, il componente non carica nuove immagini durante il ridimensionamento e la risoluzione immagine nella vista a comparsa non cambia. </p> <p>Impostato su <span class="codeph"> 1 </span> consente di specificare uno o più punti di interruzione di larghezza per l'immagine caricata nella visualizzazione principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Punto di interruzione <span class="codeph">, <span class="varname"> larghezza </span>; <span class="varname"> larghezza </span> </span> </p> </td> 
   <td colname="col2"> <p>Punti di interruzione di larghezza per l'immagine caricata nella visualizzazione principale. </p> <p>Il componente utilizza sempre le dimensioni migliori per il caricamento iniziale. Dopo il ridimensionamento, l’immagine nella vista principale viene sempre scaricata con una larghezza pari al punto di interruzione più vicino e quindi ridimensionata sul client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
