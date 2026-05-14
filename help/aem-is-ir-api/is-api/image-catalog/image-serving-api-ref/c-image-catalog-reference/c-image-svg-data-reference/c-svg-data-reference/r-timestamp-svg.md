---
description: Timestamp
solution: Experience Manager
title: Timestamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36660bb-d2ec-464c-b578-fe862bca5c50
TQID: 'https://experienceleague.adobe.com/n-LXS-OEhuBOkse44eQ0HTHV-Bx5BRH3AjgE0xInqK8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 200
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
