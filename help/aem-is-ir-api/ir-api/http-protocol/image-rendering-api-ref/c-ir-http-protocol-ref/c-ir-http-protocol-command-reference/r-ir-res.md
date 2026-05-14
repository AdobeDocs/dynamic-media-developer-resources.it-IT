---
title: res
description: Risoluzione del materiale. Specifica la risoluzione della texture o dell'immagine di decalcomania ripetibile.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f207355d-5819-47fc-bda5-27a411449569
TQID: 'https://experienceleague.adobe.com/F-ow5-VFHuZFZ7F-v3csRKFxospULbiR2bDpqbvUaYc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 105
ht-degree: 2%

---

# res{#res}

Risoluzione del materiale. Specifica la risoluzione della texture o dell&#39;immagine di decalcomania ripetibile.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> Valore <span class="varname"> </span> </p> </td> 
  <td class="stentry"> <p>Risoluzione; unità di risoluzione del materiale (tipicamente pixel per pollice) (reale). </p> </td> 
 </tr> 
</table>

Se è presente un materiale di decalcomania, `size=` prevale se sono specificati sia `size=` che `res=`.

## Proprietà {#section-6a458ddc202f46e0b668c9f040a65cef}

Attributo materiale. Ignorato dai materiali a colori. Solo con i materiali di rivestimento di armadi e finestre solo se viene utilizzata anche una texture.

## Predefinito {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, se il materiale è basato su una voce di catalogo, altrimenti `attribute::Resolution`, se `res= is` non è specificato o impostato su un valore minore o uguale a 0.

## Consultate anche {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Risoluzione materiale](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b), [dimensione=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988), [catalogo::Risoluzione](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7), [attributo::Risoluzione](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
