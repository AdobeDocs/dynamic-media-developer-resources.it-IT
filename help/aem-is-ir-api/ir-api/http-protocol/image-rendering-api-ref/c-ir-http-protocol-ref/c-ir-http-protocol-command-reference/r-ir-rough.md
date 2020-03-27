---
description: Rugosità della superficie del materiale. Specifica la rugosità relativa della superficie del materiale.
seo-description: Rugosità della superficie del materiale. Specifica la rugosità relativa della superficie del materiale.
seo-title: grezzo
solution: Experience Manager
title: grezzo
topic: Scene7 Image Serving - Image Rendering API
uuid: d3b4ece1-cc2a-4012-ad81-2f313d3a370b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# grezzo{#rough}

Rugosità della superficie del materiale. Specifica la rugosità relativa della superficie del materiale.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>rugosità superficie (0...100%) o -1 per selezionare la rugosità predefinita. </p> </td> 
 </tr> 
</table>

Utilizzato per controllare l&#39;effetto di rendering del riflesso 3D. Valori di rugosità inferiori producono in genere effetti di riflessione più omogenei; valori più elevati causano la randomizzazione e la dispersione dell’immagine riflessa.

Ciascun tipo di materiale ( `type=`) definisce un effetto di rendering minimo e massimo basato sulla rugosità. Per alcuni tipi di materiali (ad esempio la carta da parete), `rough=` ha un impatto minimo sull&#39;aspetto della riflessione, mentre per altri tipi di materiali (ad esempio pietra o ceramica) l&#39;effetto è sostanzialmente più pronunciato.

`rough=-1` imposta la rugosità su un valore predefinito interno al server (40% per i tipi di materiale tipici).

## Proprietà {#section-515375758b254c80af576271bdb61bb8}

Attributo materiale. Ignorato se la vignettatura non dispone di capacità di riflessione 3D, se all&#39;oggetto di destinazione non è associata una geometria 3D, o se l&#39;oggetto di destinazione non riflette altri oggetti nella scena.

## Predefinito {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` se il materiale è basato su una voce di catalogo, altrimenti circa il 40%.

## Consultate anche {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
