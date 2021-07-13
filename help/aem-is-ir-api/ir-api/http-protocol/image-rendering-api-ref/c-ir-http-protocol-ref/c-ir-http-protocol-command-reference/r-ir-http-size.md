---
description: Dimensione del carrello. Specifica le dimensioni di un materiale decal.
solution: Experience Manager
title: size
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 2%

---

# size{#size}

Dimensione del carrello. Specifica le dimensioni di un materiale decal.

` size= *`larghezza,altezza`*[ *`,spessore`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> larghezza, altezza  </span> </p> </td> 
  <td class="stentry"> <p>Dimensioni dell'oggetto decal nelle unità di coordinate della scena (tipicamente pollici) (reale, reale). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> spessore  </span> </p> </td> 
  <td class="stentry"> <p>Spessore dell'oggetto decal nelle unità di coordinate della scena (tipicamente pollici) (reale). </p> </td> 
 </tr> 
</table>

Se né la larghezza né l’altezza sono pari a 0, l’immagine viene ridimensionata in base alle dimensioni specificate e le proporzioni dell’immagine non vengono mantenute. Impostando uno dei due valori su 0 si conservano le proporzioni dell&#39;immagine.

Se è specificato *`thickness`*, viene eseguito il rendering di un’ombreggiatura se l’oggetto vignetta definisce un vettore di luce appropriato. Imposta *`thickness`* su 0 per disabilitare il rendering dell&#39;ombra esterna.

## Proprietà {#section-818e01e91fed4015951189c818ef28d8}

Attributo materiale. Utilizzato solo da caldaie; ignorato da tutti gli altri materiali. `res=` viene ignorato se larghezza o altezza è maggiore di 0. I valori non devono essere negativi.

## Predefinito {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` se il materiale del decal si basa su una voce del catalogo; altrimenti  `size=0,0,0`. La dimensione del decal viene calcolata a partire da `res=` se *`wid`* e *`hei`* non sono specificati o sono impostati su 0. Se *`thickness`* non è specificato o impostato su 0, non viene eseguito il rendering di alcuna ombreggiatura esterna.

## Esempio {#section-04fdc2b60b9e4071b672bf6a913738ad}

Un MSS per un decal, che è dimensionato in base alla risoluzione, ruotato di 20 gradi in senso orario, e ha uno spessore di 2,5 pollici, per un effetto di ombra esterna appropriato:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Consultate anche {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordinate](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1) scena,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04),  [attributo::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
