---
title: FlyoutZoomView.imagereload
description: Configura il modo in cui il componente recupera le nuove immagini per la visualizzazione principale e a comparsa durante il ridimensionamento.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
TQID: 'https://experienceleague.adobe.com/vyA-GdKo06kVi3jO6wlBIyov3XvKVo1vwPj3mzqyoc4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configura il modo in cui il componente recupera le nuove immagini per la visualizzazione principale e a comparsa durante il ridimensionamento.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`larghezza`*[; *`larghezza`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p>Se è impostato su <span class="codeph"> 0 </span>, il componente non carica nuove immagini durante il ridimensionamento e la risoluzione dell'immagine nella visualizzazione a comparsa non cambia. </p> <p>Se è impostato su <span class="codeph"> 1 </span>, è possibile specificare uno o più punti di interruzione di larghezza per l'immagine caricata nella visualizzazione principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Punto di interruzione <span class="codeph">, <span class="varname"> larghezza </span>[; <span class="varname"> larghezza </span>] </span> </p> </td> 
   <td colname="col2"> <p>Punti di interruzione di larghezza per l’immagine caricata nella vista principale. Il componente utilizza sempre le dimensioni migliori per il caricamento iniziale. Dopo il ridimensionamento, l’immagine nella vista principale viene sempre scaricata con la larghezza pari al punto di interruzione più grande più vicino e ridimensionata sul client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
