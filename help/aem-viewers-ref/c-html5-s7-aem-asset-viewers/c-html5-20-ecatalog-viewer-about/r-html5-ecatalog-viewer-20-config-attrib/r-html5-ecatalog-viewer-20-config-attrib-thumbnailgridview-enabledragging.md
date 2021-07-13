---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,User
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> Abilita o disabilita lo scorrimento dei campioni con il mouse o mediante movimenti touch </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> Funzioni all'interno dell'intervallo <span class="codeph"> 0-1 </span>. Si tratta di un valore <span class="codeph"> % </span> per il movimento nella direzione sbagliata della velocità effettiva. Se è impostato su <span class="codeph"> 1 </span>, si sposta con il mouse. Se è impostato su <span class="codeph"> 0 </span>, non consente di spostarsi nella direzione sbagliata. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-831c23dea82449bfa50fd155bea365b7}

Facoltativo.

## Predefinito {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## Esempio {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
