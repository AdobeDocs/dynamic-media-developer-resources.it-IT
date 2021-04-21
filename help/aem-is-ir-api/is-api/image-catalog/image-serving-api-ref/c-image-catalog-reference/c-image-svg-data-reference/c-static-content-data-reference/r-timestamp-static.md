---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# TimeStamp{#timestamp}

Se è impostato `attribute::UseLastModified`, il valore `catalog::TimeStamp` viene restituito nella risposta HTTP come intestazione HTTP Last-Modified. L’intestazione Last-Modified viene sempre restituita per i contenuti statici, anche se `attribute::UseLastModified` non è impostato.

Per immagini e contenuti SVG, `catalog::TimeStamp` viene utilizzato anche per la convalida della cache basata su catalogo (vedi ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`).

## Proprietà {#section-2298a384b5cb43929542655c5a49beb2}

Valore data/ora in formato Java. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, dal 1° gennaio 1970 UTC/GMT oppure un valore di stringa data/ora con uno dei seguenti formati:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* è compreso tra 0 e 23.

*`zzz`* è un codice del fuso orario a tre o quattro caratteri come &quot;GMT&quot; o &quot;PST&quot;. Conto per ora legale nel codice del fuso orario. Ad esempio, &quot;PST&quot; per l’ora standard del Pacifico, rispetto a &quot;PDT&quot; per l’ora legale del Pacifico).

*`offset`* è un offset del fuso orario in ore o  `hours:minutes`, relativo a GMT. Ad esempio, &quot;PDT&quot; equivale a &quot;GMT -7&quot;.

Tutti gli elementi dei valori data/ora formattati in stringa devono essere presenti. Se il valore data/ora non viene formattato correttamente, viene ignorato e viene invece utilizzata l&#39;ora di modifica del file `*`catalog`*.ini` .

## Predefinito {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` se il campo è vuoto o non è presente.

## Consultate anche {#section-c42a427aa4794c548408dc4de028d578}

[attributo::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296),  [attributo::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attributo::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
