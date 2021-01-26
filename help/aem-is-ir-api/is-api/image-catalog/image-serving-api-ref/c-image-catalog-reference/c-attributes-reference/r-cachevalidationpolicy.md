---
description: Criterio di convalida della cache del server. Specifica quando le voci della cache lato server vengono convalidate.
seo-description: Criterio di convalida della cache del server. Specifica quando le voci della cache lato server vengono convalidate.
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 371dadbf-d58e-4214-8050-7e8907b436e3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

Criterio di convalida della cache del server. Specifica quando le voci della cache lato server vengono convalidate.

Con la convalida basata sulla scadenza, le immagini sorgente vengono verificate periodicamente se sono state modificate o meno. Con la convalida basata su catalogo, le immagini sorgente vengono controllate solo dopo la modifica del valore `catalog::TimeStamp`.

Quando si utilizzano i cataloghi di immagini, si consiglia di eseguire una convalida basata su catalogo. La convalida basata sulla scadenza deve essere utilizzata quando alle immagini viene fatto riferimento direttamente, senza l’utilizzo di un catalogo immagini.

## Proprietà {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 per selezionare la convalida basata sulla scadenza, 1 per selezionare la convalida della cache basata sul catalogo.

## Predefinito {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Ereditato da `default::CacheValidationPolicy` se non definito o se vuoto.

## Consultate anche {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
