---
title: IccRenderIntent
description: Intento di rendering della conversione del colore. Fornisce l'intento di rendering predefinito per le conversioni di colore quando l'intento di rendering non è specificato con icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 4%

---

# IccRenderIntent{#iccrenderintent}

Intento di rendering della conversione del colore. Fornisce l&#39;intento di rendering predefinito per le conversioni di colore quando l&#39;intento di rendering non è specificato con `icc=`.

## Proprietà {#section-0a38c60e1525426185616c42824aee2c}

Enum. Impostato su 0 per percettivo, 1 per colorimetrico relativo, 2 per saturazione, 3 per colorimetrico assoluto. Mantieni vuoto o impostato su qualsiasi altro valore per utilizzare l’intento di rendering predefinito definito nel profilo colore.

## Predefinito {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Ereditato da `default::IccRenderIntent`se non definito. Se vuoto, viene applicato il valore &quot;colorimetrico relativo&quot;.

## Consultate anche {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attributo::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [attributo::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
