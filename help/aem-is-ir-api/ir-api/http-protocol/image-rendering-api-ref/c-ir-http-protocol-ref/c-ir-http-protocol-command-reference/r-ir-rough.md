---
description: Rugosità della superficie del materiale. Specifica la rugosità relativa della superficie del materiale.
solution: Experience Manager
title: ruvido
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# grezzo{#rough}

Rugosità della superficie del materiale. Specifica la rugosità relativa della superficie del materiale.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Rugosità della superficie (0...100%) o -1 per selezionare la rugosità predefinita. </p> </td> 
 </tr> 
</table>

Utilizzato per controllare l&#39;effetto di rendering del riflesso 3D. Valori di rugosità inferiori producono tipicamente effetti di riflessione più uniformi; valori più alti causano la randomizzazione e la dispersione dell&#39;immagine riflessa.

Ogni tipo di materiale ( `type=`) definisce un effetto di rendering minimo e massimo di riflessione in base alla rugosità. Per alcuni tipi di materiale (ad esempio carta da parete), `rough=` non ha praticamente alcun impatto sull&#39;aspetto del riflesso, mentre per altri tipi di materiale (ad esempio pietra o ceramica), l&#39;effetto è sostanzialmente più pronunciato.

`rough=-1` imposta la rugosità su un valore predefinito interno al server (40% per i tipi di materiale tipici).

## Proprietà {#section-515375758b254c80af576271bdb61bb8}

Attributo materiale. Ignorato se la vignetta non ha alcuna funzionalità di riflessione 3D, se all’oggetto di destinazione non è associata una geometria 3D, o se l’oggetto di destinazione non riflette altri oggetti della scena.

## Predefinito {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` se il materiale è basato su una voce di catalogo, altrimenti circa il 40%.

## Consultate anche {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) ,  [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
