---
title: lucentezza
description: Lucidità della superficie del materiale. Specifica la lucentezza relativa della superficie del materiale. Consente di selezionare la mappa di illuminazione e controllare il rendering degli effetti di lucentezza e dei riflessi 3D.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# lucentezza{#gloss}

Lucidità della superficie del materiale. Specifica la lucentezza relativa della superficie del materiale. Consente di selezionare la mappa di illuminazione e controllare il rendering degli effetti di lucentezza e dei riflessi 3D.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>brillantezza (0...100 percento) o -1 per il valore di default (di riferimento) della brillantezza. </p></td> 
 </tr> 
</table>

Valori di brillantezza più alti causano solitamente riflessi più forti e netti e, se gli effetti di brillantezza sono attivati nella vignettatura, rafforzano le luci speculari sulla superficie materiale, soprattutto aumentando il contrasto dell&#39;illuminazione. Ogni tipo di materiale ( `type=`) definisce un effetto di rendering minimo e massimo. Per alcuni tipi di materiale (ad esempio, carta da parati), `gloss=` ha un impatto minimo sull&#39;aspetto dell&#39;effetto di rendering, mentre per altri tipi di materiale (ad esempio, pietra o ceramica), l&#39;effetto è sostanzialmente più pronunciato.

Se `illum=-1` e se la vignettatura definisce mappe di illuminazione multipla, `gloss=` seleziona la mappa di illuminazione utilizzata per l&#39;operazione di rendering corrente. Il renderer sceglie la mappa di illuminazione il cui valore di lucentezza è più vicino alla lucentezza specificata.

`gloss=-1` Seleziona il valore di riferimento della mappa di illuminazione selezionata, come definito nelle proprietà di visualizzazione della vignettatura. Questo valore assicura che la mappa di illuminazione venga utilizzata esattamente come è stata creata, senza ulteriori modifiche, anche se gli effetti di lucentezza sono attivati. Se `illum=-1` viene quindi utilizzato il valore di riferimento della prima mappa di illuminazione nella vista vignettatura.

## Proprietà {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Attributo materiale. Ignorato se la vignettatura non definisce mappe di illuminazione multiple. Oppure, se `illum=` se la vignettatura non include dati di riflessione 3D. Oppure, se l&#39;oggetto corrente non supporta riflessi 3D o se gli effetti di lucentezza sono disattivati nella vignettatura.

## Predefinito {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` Se il materiale è basato su una voce di catalogo, altrimenti il valore di riferimento della mappa di illuminazione di default o della mappa di illuminazione specificata da `illum=`.

## Consultate anche {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [ruvido=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
