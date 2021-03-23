---
description: Risoluzione del materiale. Specifica la risoluzione della texture o dell'immagine decal ripetibili.
seo-description: Risoluzione del materiale. Specifica la risoluzione della texture o dell'immagine decal ripetibili.
seo-title: res
solution: Experience Manager
title: res
uuid: ae755a92-ad06-4cf2-b627-0b8b14e385c3
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---


# res{#res}

Risoluzione del materiale. Specifica la risoluzione della texture o dell&#39;immagine decal ripetibili.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Risoluzione; unità di risoluzione del materiale (in genere pixel per pollice) (reale). </p> </td> 
 </tr> 
</table>

Nel caso di un materiale decal, prevale `size=` se sono specificati sia `size=` che `res=`.

## Proprietà {#section-6a458ddc202f46e0b668c9f040a65cef}

Attributo materiale. Ignorato da materiali a colori solidi. Solo con materiali di rivestimento per mobili e finestre solo se viene utilizzata anche una texture.

## Predefinito {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, se il materiale è basato su una voce di catalogo, altrimenti  `attribute::Resolution`se  `res= is` non specificato o impostato su un valore minore o uguale a 0.

## Consultate anche {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Risoluzione](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b) materiale,  [dimensione=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988),  [catalogo::Risoluzione](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7),  [attributo::Risoluzione](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
