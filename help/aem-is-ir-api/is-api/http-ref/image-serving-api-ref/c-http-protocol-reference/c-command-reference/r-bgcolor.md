---
description: Colore sfondo livello. Specifica il colore e l'opacità dello sfondo del livello corrente.
solution: Experience Manager
title: bgColor
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 22c957e6-1a82-43a7-8467-871a150e7453
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---

# bgColor{#bgcolor}

Colore sfondo livello. Specifica il colore e l&#39;opacità dello sfondo del livello corrente.

`bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span></span> </p> </td> 
  <td class="stentry"> <p>Valore del colore grigio, RGB o CMYK, con o senza alfa. </p></td> 
 </tr> 
</table>

Le aree trasparenti e semiopache all’interno del rettangolo di delimitazione del livello vengono riempite con il colore specificato* dopo l’applicazione dei valori* `opac=`, `rotate=` e `extend=`.

## Proprietà {#section-19dfc13e997f4a33889a1df1e4ad50b9}

Attributo livello. Si applica al livello corrente o al livello 0 se `layer=comp`. Ignorato dai livelli di effetto.

*`color`* si presume che esista nello spazio colore di lavoro corrispondente al tipo di pixel di  *`color`*. *`color`* viene convertito con precisione se l&#39;immagine del livello finale ha un tipo di pixel diverso.

## Predefinito {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0 (completamente trasparente).

## Esempio {#section-6e14fcf1d31e432dbdb56b9320904453}

Vedere [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423).

## Consultate anche {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423),  [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [Gestione colore](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
