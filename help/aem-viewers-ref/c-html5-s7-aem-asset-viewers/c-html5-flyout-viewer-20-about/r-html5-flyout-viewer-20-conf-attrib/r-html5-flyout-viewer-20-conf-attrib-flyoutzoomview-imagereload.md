---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
TQID: 'https://experienceleague.adobe.com/nkYQwtTb1AUBLBbnN2HwMZLIjyolj5l-6CxEy-yEo3k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`larghezza`*[; *`larghezza`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Configura il modo in cui il componente recupera le nuove immagini per la visualizzazione principale e a comparsa durante il ridimensionamento. </p> <p>Se è impostato su <span class="codeph"> 0 </span>, il componente non carica nuove immagini durante il ridimensionamento; la risoluzione dell'immagine nella vista a comparsa non cambia. </p> <p>L'impostazione su <span class="codeph"> 1 </span> consente di specificare uno o più punti di interruzione di larghezza per l'immagine caricata nella visualizzazione principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Punto di interruzione <span class="codeph">, <span class="varname"> larghezza </span>[; <span class="varname"> larghezza </span>] </span> </p> </td> 
   <td colname="col2"> <p> Punti di interruzione di larghezza per l'immagine caricata nella visualizzazione principale. Il componente utilizza sempre le dimensioni migliori per il caricamento iniziale. Dopo il ridimensionamento, l’immagine nella vista principale viene sempre scaricata con la larghezza uguale al punto di interruzione più grande più vicino e ridimensionata sul client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
