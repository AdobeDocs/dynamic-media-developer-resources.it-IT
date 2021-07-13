---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`Sensibilitàx`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Sensibilità</span>[,  <span class="varname"> sensibilità</span>]</span> </p> </td> 
   <td colname="col2"> <p> Controlla la sensibilità della rotazione orizzontale e verticale eseguita con un trascinamento del mouse o un passaggio del mouse. </p> <p> <span class="codeph"> </span> xSensitivityimposta quante rotazioni di prodotto orizzontali vengono effettuate se l'utente trascina il mouse in orizzontale da un lato all'altro della visualizzazione. Ad esempio, tre significa che l’utente visualizza tre giri completi per un gesto di trascinamento completo. </p> <p>Allo stesso modo, <span class="codeph"> Sensibilità</span> controlla la sensibilità della rotazione verticale. Un valore pari a 1 indica che un trascinamento verticale completo cambia l’angolo di visualizzazione dal piano di rotazione più in alto a quello più in basso (o viceversa). </p> <p>Impostando un valore negativo per <span class="codeph"> ySensitive</span> si inverte la direzione della rotazione verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
