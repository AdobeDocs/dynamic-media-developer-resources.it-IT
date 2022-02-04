---
title: FlyoutZoomView.imagereload
description: Configura il modo in cui il componente recupera le nuove immagini per la vista principale e a comparsa durante il ridimensionamento.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configura il modo in cui il componente recupera le nuove immagini per la vista principale e a comparsa durante il ridimensionamento.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`larghezza`*[; *`larghezza`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>Quando è impostato su <span class="codeph"> 0 </span>, il componente non carica nuove immagini durante il ridimensionamento e la risoluzione dell’immagine nella visualizzazione a comparsa non cambia. </p> <p>Quando è impostato su <span class="codeph"> 1 </span> consente di specificare uno o più punti di interruzione della larghezza per l’immagine caricata nella vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> punto di interruzione, <span class="varname"> larghezza </span>[; <span class="varname"> larghezza </span>] </span> </p> </td> 
   <td colname="col2"> <p>Punti di interruzione della larghezza per l’immagine caricata nella vista principale. Il componente utilizza sempre le dimensioni di adattamento migliori per il caricamento iniziale. Dopo il ridimensionamento, l’immagine nella vista principale viene sempre scaricata con la larghezza uguale al punto di interruzione più vicino e ridimensionata sul client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
