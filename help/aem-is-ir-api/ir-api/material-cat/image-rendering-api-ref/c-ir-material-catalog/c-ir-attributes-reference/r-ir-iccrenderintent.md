---
description: Intento di rendering della conversione del colore. Fornisce l'intento di rendering predefinito per le conversioni di colore quando l'intento di rendering non è specificato con icc=.
seo-description: Intento di rendering della conversione del colore. Fornisce l'intento di rendering predefinito per le conversioni di colore quando l'intento di rendering non è specificato con icc=.
seo-title: IccRenderIntent
solution: Experience Manager
title: IccRenderIntent
topic: Scene7 Image Serving - Image Rendering API
uuid: a9648405-32c3-4762-bbb2-11e97d4f8374
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# IccRenderIntent{#iccrenderintent}

Intento di rendering della conversione del colore. Fornisce l&#39;intento di rendering predefinito per le conversioni di colore quando l&#39;intento di rendering non è specificato con icc=.

## Proprietà {#section-0a38c60e1525426185616c42824aee2c}

Enum. Impostato su 0 per la percezione, 1 per la colorimetria relativa, 2 per la saturazione, 3 per la colorimetria assoluta. Mantenete vuoto o impostate su qualsiasi altro valore per utilizzare l’intento di rendering predefinito definito nel profilo colore.

## Predefinito {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Ereditato da `default::IccRenderIntent`se non definito. Se vuoto, viene applicato il colorimetrico relativo.

## Consultate anche {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attributo::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ,  [attributo::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
