---
title: SpinView.zoomstep
description: SpinView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: afc2018f-b222-4fd5-b9dc-88655793efd4
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *`step`*[, *`limite`*]`

<table id="table_2D7F971D503348B8A9559362A1D9B26D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p> Configura le azioni di zoom in e zoom out necessarie per aumentare o ridurre la risoluzione di un fattore di due. La modifica della risoluzione per ogni azione di zoom è di 2^1 per passo. Imposta su <span class="codeph"> 0</span> per eseguire lo zoom a piena risoluzione con una singola azione zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limite</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica la risoluzione massima dello zoom rispetto all'immagine a risoluzione piena. Il valore predefinito è <span class="codeph"> 1,0</span>, che non consente di ingrandire oltre la risoluzione completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
