---
title: Timestamp
description: Se è impostato "attribute::UseLastModified", il valore "catalog::TimeStamp" viene restituito nella risposta HTTP come intestazione HTTP Last-Modified.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# Timestamp{#timestamp}

Se `attribute::UseLastModified` è impostato, il `catalog::TimeStamp` Il valore viene restituito nella risposta HTTP come intestazione HTTP Last-Modified. L’intestazione Ultima modifica viene sempre restituita per i contenuti statici, anche se `attribute::UseLastModified` non è impostato.

Per i contenuti di immagini e SVG, `catalog::TimeStamp` viene utilizzato anche per la convalida della cache basata su catalogo (vedi [attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Proprietà {#section-2298a384b5cb43929542655c5a49beb2}

Valore data/ora in formato Java. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, 1 gennaio 1970 UTC/GMT, o un valore stringa data/ora con uno dei seguenti formati:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* è compreso tra 0 e 23.

*`zzz`* è un codice di fuso orario di tre o quattro caratteri, ad esempio &#39;GMT&#39; o &#39;PST&#39;. Account per l’ora legale nel codice del fuso orario. Ad esempio, &#39;PST&#39; per l&#39;ora solare del Pacifico rispetto a &#39;PDT&#39; per l&#39;ora legale del Pacifico).

*`offset`* è uno scostamento del fuso orario in ore o `hours:minutes`, relativo a GMT. Ad esempio, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Tutti gli elementi dei valori di data/ora in formato stringa devono essere presenti. Se il valore data/ora non è formattato correttamente, viene ignorato e l’ora di modifica del `*`catalogo`*.ini` al suo posto viene utilizzato il file.

## Predefinito {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` se il campo è vuoto o non presente.

## Consultate anche {#section-c42a427aa4794c548408dc4de028d578}

[attribute::Timestamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
