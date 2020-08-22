---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 98a84ba1-4b89-424a-ac2e-4a59af33cec0
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`larghezza`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Configura il modo in cui il componente recupera le nuove immagini per la visualizzazione principale e a comparsa durante il ridimensionamento. </p> <p>Con <span class="codeph"> 0 </span>, il componente non carica nuove immagini durante il ridimensionamento e la risoluzione delle immagini nella visualizzazione a comparsa non cambia. </p> <p>Impostato su <span class="codeph"> 1 </span> , potete specificare uno o più punti di interruzione di larghezza per l’immagine caricata nella vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> punto di interruzione, <span class="varname"> larghezza </span>; <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p>Punti di interruzione della larghezza per l’immagine caricata nella vista principale. </p> <p>Il componente utilizza sempre le dimensioni di adattamento migliori per il caricamento iniziale. Dopo il ridimensionamento, l’immagine nella vista principale viene sempre scaricata con la larghezza uguale al punto di interruzione più grande più vicino e ridimensionata sul client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
