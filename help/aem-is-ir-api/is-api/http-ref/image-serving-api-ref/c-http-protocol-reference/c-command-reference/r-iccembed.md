---
description: Incorpora profilo colore. Specifica se il profilo colore ICC di lavoro o il profilo specificato con icc= devono essere incorporati nell'immagine di risposta.
seo-description: Incorpora profilo colore. Specifica se il profilo colore ICC di lavoro o il profilo specificato con icc= devono essere incorporati nell'immagine di risposta.
seo-title: iccEmbed
solution: Experience Manager
title: iccEmbed
uuid: ccd3fd2f-6f73-4725-a51a-9daf643d71af
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# iccEmbed{#iccembed}

Incorpora profilo colore. Specifica se il profilo colore ICC di lavoro o il profilo specificato con icc= devono essere incorporati nell&#39;immagine di risposta.

`iccEmbed=0|1`

## Proprietà {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Attributo di richiesta. Ignorato se non è disponibile alcun profilo per l’incorporazione.

## Predefinito {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`, per non incorporare profili ICC nelle immagini di output. Ignorato se il formato immagine di output non supporta l’incorporazione di profili ICC.

Per ulteriori informazioni, vedere [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) .

## Consultate anche {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attributo::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ,  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
