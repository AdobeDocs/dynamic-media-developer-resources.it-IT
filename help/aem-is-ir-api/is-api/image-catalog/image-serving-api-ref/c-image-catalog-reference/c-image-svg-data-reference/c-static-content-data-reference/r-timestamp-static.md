---
title: Timestamp
description: Se è impostato "attribute::UseLastModified", il valore "catalog::TimeStamp" viene restituito nella risposta HTTP come intestazione HTTP Last-Modified. L’intestazione Last-Modified viene sempre restituita per i contenuti statici, anche se "attribute::UseLastModified" non è impostato.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3c47b14d-b629-474d-952a-b09e1b1162b4
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 1%

---

# Timestamp{#timestamp}

Se `attribute::UseLastModified` è impostato, il valore `catalog::TimeStamp` viene restituito nella risposta HTTP come intestazione HTTP Last-Modified. L&#39;intestazione Ultima modifica viene sempre restituita per il contenuto statico, anche se `attribute::UseLastModified` non è impostato.

Per il contenuto di immagini e SVG, `catalog::TimeStamp` viene utilizzato anche per la convalida della cache basata su catalogo (vedere [attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Proprietà {#section-2298a384b5cb43929542655c5a49beb2}

Valore data/ora in formato Java. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, 1 gennaio 1970 UTC/GMT, o un valore stringa data/ora con uno dei seguenti formati:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* è compreso tra 0 e 23.

*`zzz`* è un codice di fuso orario di tre o quattro caratteri come &#39;GMT&#39; o &#39;PST&#39;. Account per l’ora legale nel codice del fuso orario. Ad esempio, &#39;PST&#39; per l&#39;ora solare del Pacifico rispetto a &#39;PDT&#39; per l&#39;ora legale del Pacifico).

*`offset`* è una differenza di fuso orario in ore o `hours:minutes`, relativa a GMT. Ad esempio, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Tutti gli elementi dei valori di data/ora in formato stringa devono essere presenti. Se il valore data/ora non è formattato correttamente, viene ignorato e viene utilizzata l&#39;ora di modifica del file `*`catalog`*.ini`.

## Predefinito {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` se il campo è vuoto o non presente.

## Consultate anche {#section-c42a427aa4794c548408dc4de028d578}

[attributo::Timestamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attributo::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attributo::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
