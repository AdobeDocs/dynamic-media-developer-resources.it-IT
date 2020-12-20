---
description: Lucidità della superficie del materiale. Specifica la lucentezza relativa della superficie del materiale. Utilizzato per selezionare la mappa di illuminazione e controllare il rendering degli effetti lucidi e riflessi 3D.
seo-description: Lucidità della superficie del materiale. Specifica la lucentezza relativa della superficie del materiale. Utilizzato per selezionare la mappa di illuminazione e controllare il rendering degli effetti lucidi e riflessi 3D.
seo-title: lucidità
solution: Experience Manager
title: lucidità
topic: Scene7 Image Serving - Image Rendering API
uuid: 3774e08b-d24e-4cf2-8719-32a21bb9bcb6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# gloss{#gloss}

Lucidità della superficie del materiale. Specifica la lucentezza relativa della superficie del materiale. Utilizzato per selezionare la mappa di illuminazione e controllare il rendering degli effetti lucidi e riflessi 3D.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Gloss (0...100 per cento) o -1 per il valore globale predefinito (riferimento). </p></td> 
 </tr> 
</table>

Valori più alti della superficie lucida provocano generalmente riflessi più forti e più nitidi e, se nella vignettatura sono attivati effetti lucidi, rafforza le luci speculari sulla superficie del materiale, principalmente aumentando il contrasto di illuminazione. Ogni tipo di materiale ( `type=`) definisce un effetto di rendering minimo e massimo. Per alcuni tipi di materiali (ad esempio la carta da parete), `gloss=` non ha praticamente alcun impatto sull&#39;aspetto dell&#39;effetto di rendering, mentre per altri tipi di materiali (ad esempio pietra o ceramica) l&#39;effetto è sostanzialmente più pronunciato.

Se `illum=-1` e la vignettatura definisce più mappe di illuminazione, `gloss=` seleziona la mappa di illuminazione utilizzata per l&#39;operazione di rendering corrente. Il renderer sceglie la mappa di illuminazione il cui valore globale è più vicino alla superficie specificata.

`gloss=-1` seleziona il valore lucido di riferimento della mappa di illuminazione selezionata, come definito nelle proprietà di visualizzazione della vignettatura. Questo assicura che la mappa di illuminazione sia utilizzata esattamente come è stata creata, senza ulteriori modifiche, anche se gli effetti di luce sono attivati. Se anche `illum=-1`, viene utilizzato il valore lucido di riferimento della prima mappa di illuminazione nella vista vignettatura.

## Proprietà {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Attributo materiale. Ignorato se la vignettatura non definisce mappe di illuminazione multiple o se è specificato `illum=`, se la vignettatura non include dati di riflessione 3D o se l&#39;oggetto corrente non supporta riflessi 3D, o se gli effetti di globo sono disattivati nella vignettatura.

## Predefinito {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` se il materiale è basato su una voce di catalogo, altrimenti il valore lucido di riferimento della mappa di illuminazione predefinita o della mappa di illuminazione specificata da  `illum=`.

## Consultate anche {#section-29f5b761481a4c52a499a2e16e63c70b}

[attributo::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb),  [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35),  [grezzo=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180),  [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a),  [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
