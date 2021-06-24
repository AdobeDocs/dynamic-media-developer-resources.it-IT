---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: fd432573-677f-4c46-9cc1-88089496ce75
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

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

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,0.5`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enabledragging=0`
