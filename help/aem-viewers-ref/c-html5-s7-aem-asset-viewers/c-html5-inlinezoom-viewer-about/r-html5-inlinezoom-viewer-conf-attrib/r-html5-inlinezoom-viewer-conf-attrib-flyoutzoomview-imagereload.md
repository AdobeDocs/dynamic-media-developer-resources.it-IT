---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
uuid: 98a84ba1-4b89-424a-ac2e-4a59af33cec0
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom in linea
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`Larghezza `*[; *``*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Configura il modo in cui il componente recupera le nuove immagini per la vista principale e a comparsa durante il ridimensionamento. </p> <p>Impostato su <span class="codeph"> 0 </span>, il componente non carica nuove immagini durante il ridimensionamento e la risoluzione dell'immagine nella visualizzazione a comparsa non cambia. </p> <p>Impostato su <span class="codeph"> 1 </span> consente di specificare uno o più punti di interruzione della larghezza per l'immagine caricata nella vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> punto di interruzione,  <span class="varname"> larghezza  </span>;  <span class="varname"> larghezza  </span> </span> </p> </td> 
   <td colname="col2"> <p>Punti di interruzione di larghezza per l’immagine caricata nella vista principale. </p> <p>Il componente utilizza sempre le dimensioni di adattamento migliori per il caricamento iniziale. Dopo il ridimensionamento, l’immagine nella vista principale viene sempre scaricata con la larghezza corrispondente al punto di interruzione più grande più vicino e ridimensionata sul client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
