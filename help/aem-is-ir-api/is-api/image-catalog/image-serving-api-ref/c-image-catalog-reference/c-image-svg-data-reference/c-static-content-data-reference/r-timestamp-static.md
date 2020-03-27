---
description: 'null'
seo-description: 'null'
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: fd60e5db-9219-41a8-947f-0d497b39e727
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# TimeStamp{#timestamp}

Se `attribute::UseLastModified` è impostato, il `catalog::TimeStamp` valore viene restituito nella risposta HTTP come intestazione HTTP Ultima modifica. L’intestazione Ultima modifica viene sempre restituita per i contenuti statici, anche se non `attribute::UseLastModified` è impostata.

Per le immagini e i contenuti SVG, `catalog::TimeStamp` viene utilizzato anche per la convalida della cache basata su catalogo (vedere ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`).

## Proprietà {#section-2298a384b5cb43929542655c5a49beb2}

Valore data/ora in formato Java. Può essere il numero intero di millisecondi trascorsi a partire da mezzanotte, il 1 gennaio 1970 UTC/GMT oppure un valore di stringa data/ora con uno dei seguenti formati:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* è compreso tra 0 e 23.

*`zzz`* è un codice del fuso orario composto da tre o quattro caratteri, ad esempio &#39;GMT&#39; o &#39;PST&#39;. Conto per ora legale nel codice del fuso orario. Ad esempio, &#39;PST&#39; per l&#39;ora standard del Pacifico, invece di &#39;PDT&#39; per l&#39;ora legale del Pacifico).

*`offset`* è un offset del fuso orario espresso in ore o `hours:minutes`, relativo a GMT. Ad esempio, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Devono essere presenti tutti gli elementi dei valori data/ora formattati in stringa. Se il valore data/ora non è formattato correttamente, viene ignorato e viene utilizzata l&#39;ora di modifica del file ` *`catalogo`*.ini` .

## Predefinito {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` se il campo è vuoto o non è presente.

## Consultate anche {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attributo::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attributo::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
