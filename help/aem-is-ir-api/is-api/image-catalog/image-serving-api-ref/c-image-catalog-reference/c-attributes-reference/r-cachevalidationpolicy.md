---
description: Criterio di convalida della cache del server. Specifica quando vengono convalidate le voci della cache lato server.
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Criterio di convalida della cache del server. Specifica quando vengono convalidate le voci della cache lato server.

Con la convalida basata sulla scadenza, le immagini sorgente vengono periodicamente controllate se sono state modificate. Con la convalida basata su catalogo, le immagini sorgente vengono controllate solo dopo la modifica del valore `catalog::TimeStamp`.

Quando si utilizzano cataloghi di immagini, si consiglia di eseguire una convalida basata su catalogo. La convalida basata sulla scadenza deve essere utilizzata quando si fa riferimento direttamente alle immagini senza l’utilizzo di un catalogo di immagini.

## Proprietà {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 per selezionare la convalida basata sulla scadenza, 1 per selezionare la convalida della cache basata sul catalogo.

## Predefinito {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Ereditato da `default::CacheValidationPolicy` se non definito o se vuoto.

## Consultate anche {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
