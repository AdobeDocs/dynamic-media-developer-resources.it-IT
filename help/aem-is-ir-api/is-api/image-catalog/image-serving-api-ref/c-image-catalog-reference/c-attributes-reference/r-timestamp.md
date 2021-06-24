---
description: Timestamp predefinito per la modifica dell'immagine. Fornisce un valore predefinito per TimeStamp del catalogo.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# TimeStamp{#timestamp}

Timestamp predefinito per la modifica dell&#39;immagine. Fornisce un valore predefinito per catalog::TimeStamp.

Se non viene specificato, il server utilizzerà la data/ora di modifica del file [!DNL *`catalog`*.ini].

## Proprietà {#section-647066e62ce44a84b627fdd0b2f7cfec}

Valore data/ora. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, dal 1° gennaio 1970 UTC/GMT o un valore di stringa data/ora con uno dei seguenti formati:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* è compreso tra 0 e 23.

*`zzz`* è un codice del fuso orario a 3 o 4 caratteri, ad esempio  `GMT` o  `PST`. Nel codice del fuso orario deve essere tenuto conto dell’ora legale (ad esempio `PST` per l&#39;ora standard del Pacifico, rispetto a `PDT` per l&#39;ora legale del Pacifico).

*`offset`* è un offset del fuso orario in ore o ore:minuti, relativo a GMT. Ad esempio, `PDT` equivale a `GMT -7`.

Tutti gli elementi dei valori data/ora formattati in stringa devono essere presenti. Se il valore data/ora non viene formattato correttamente, viene ignorato e viene invece utilizzata l&#39;ora di modifica del file [!DNL *`catalog`*.ini].

## Predefinito {#section-ac465313c97943ed97d41ea852329177}

Se vuoto o non definito, il server utilizza l&#39;ora di modifica del file `*`catalog`*.ini`.

## Consultate anche {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [attributo::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attributo::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
