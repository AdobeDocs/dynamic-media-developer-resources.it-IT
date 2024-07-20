---
title: dimensione
description: Dimensione decalcomania. Specifica le dimensioni di un materiale decalcomania.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# dimensione{#size}

Dimensione decalcomania. Specifica le dimensioni di un materiale decalcomania.

` size= *`larghezza,altezza`*[ *`,spessore`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> larghezza, altezza </span> </p> </td> 
  <td class="stentry"> <p>Dimensione dell'oggetto decalcomania in unità di coordinate della scena (tipicamente pollici) (reale, reale). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> spessore </span> </p> </td> 
  <td class="stentry"> <p>Spessore dell'oggetto decalcomania in unità di coordinate della scena (tipicamente pollici) (reale). </p> </td> 
 </tr> 
</table>

Se né larghezza né altezza sono uguali a 0, l&#39;immagine viene ridimensionata in base alle dimensioni specificate e le proporzioni dell&#39;immagine non vengono mantenute. Impostando entrambi i valori su 0 si mantengono le proporzioni dell&#39;immagine.

Se si specifica *`thickness`*, viene eseguito il rendering di un&#39;ombra esterna se l&#39;oggetto di vignettatura definisce un vettore di luce appropriato. Impostare *`thickness`* su 0 per disabilitare il rendering delle ombre esterne.

## Proprietà {#section-818e01e91fed4015951189c818ef28d8}

Attributo materiale. Utilizzato solo dalle decalcomanie; ignorato da tutti gli altri materiali. `res=` viene ignorato se larghezza o altezza è maggiore di 0. I valori non devono essere negativi.

## Predefinito {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` se il materiale della decalcomania è basato su una voce di catalogo; altrimenti `size=0,0,0`. La dimensione della decalcomania viene calcolata da `res=` se *`wid`* e *`hei`* non sono specificati o sono impostati su 0. Se *`thickness`* non è specificato o è impostato su 0, non viene eseguito il rendering di alcuna ombra esterna.

## Esempio {#section-04fdc2b60b9e4071b672bf6a913738ad}

MSS per una decalcomania, dimensionata in base alla risoluzione, ruotata di 20 gradi in senso orario e con uno spessore di 2,5 pollici, per un appropriato effetto ombra esterna:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Consultate anche {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordinate scene](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
