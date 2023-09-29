---
title: IccRenderIntent
description: Intento di rendering della conversione colore. Fornisce l’intento di rendering predefinito per le conversioni dei colori quando `icc=` non è specificato per l’intento di rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# IccRenderIntent{#iccrenderintent}

Intento di rendering della conversione colore. Specifica l&#39;intento di rendering predefinito per le conversioni di colore quando l&#39;intento di rendering non è specificato con `icc=`.

## Proprietà {#section-2540099fb2fc47d29b04642da4f5922a}

Enum. Impostate questo valore su 0 per percettivo, 1 per colorimetrico relativo, 2 per saturazione, 3 per colorimetrico assoluto.

## Predefinito {#section-61a05067905b44099c228e15de279dbd}

Ereditato da `default::IccRenderIntent` se non è definita o se è vuota.

## Consultate anche {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;, [attribute::Compensazione punto nero Icc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
