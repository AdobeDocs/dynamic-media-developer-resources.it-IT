---
description: Configura il modo in cui il componente recupera le nuove immagini per la visualizzazione principale e a comparsa durante il ridimensionamento.
seo-description: Configura il modo in cui il componente recupera le nuove immagini per la visualizzazione principale e a comparsa durante il ridimensionamento.
seo-title: FlyoutZoomView.imagerload
solution: Experience Manager
title: FlyoutZoomView.imagerload
topic: Dynamic media
uuid: 5cded4cb-7b02-47da-9e2d-b236548cc61d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.imagerload{#flyoutzoomview-imagereload}

Configura il modo in cui il componente recupera le nuove immagini per la visualizzazione principale e a comparsa durante il ridimensionamento.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`larghezza`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>Se è impostato su <span class="codeph"> 0 </span>, il componente non carica le nuove immagini durante il ridimensionamento e la risoluzione delle immagini nella visualizzazione a comparsa non cambia. </p> <p>Se è impostato su <span class="codeph"> 1, </span> è possibile specificare uno o più punti di interruzione di larghezza per l’immagine caricata nella vista principale. </p> </td> 
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
