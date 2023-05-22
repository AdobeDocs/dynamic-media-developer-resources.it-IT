---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensitivity`*[, *`ySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[, <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Controlla la sensibilità della rotazione orizzontale e verticale eseguita con un trascinamento del mouse. </p> <p> <span class="codeph"> xSensitivity</span> imposta il numero di rotazioni orizzontali del prodotto effettuate se l'utente trascina il mouse orizzontalmente da un lato all'altro della vista. Ad esempio, tre significa che l’utente visualizza tre rotazioni complete per un movimento di trascinamento completo. </p> <p>Analogamente, <span class="codeph"> ySensitivity</span> controlla la sensibilità della rotazione verticale. Il valore 1 indica che una traslazione verticale completa cambia l'angolo di visualizzazione dal piano di rotazione superiore a quello inferiore (o viceversa). </p> <p>Impostazione di un valore negativo per <span class="codeph"> ySensitivity</span> inverte la direzione della rotazione verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
