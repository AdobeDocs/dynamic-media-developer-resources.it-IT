---
description: Timestamp di modifica immagine predefinito. Fornisce un valore predefinito per il catalogo TimeStamp.
seo-description: Timestamp di modifica immagine predefinito. Fornisce un valore predefinito per il catalogo TimeStamp.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 0670e53a-ad7d-46cf-8e18-4c52a766df6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 2%

---


# TimeStamp{#timestamp}

Timestamp di modifica immagine predefinito. Fornisce un valore predefinito per catalog::TimeStamp.

Se non viene specificato, il server utilizzerà la data/ora di modifica del file [!DNL *`catalog`*.ini].

## Proprietà {#section-647066e62ce44a84b627fdd0b2f7cfec}

Valore data/ora. Può essere il numero intero di millisecondi trascorsi a partire da mezzanotte, il 1 gennaio 1970 UTC/GMT oppure un valore di stringa data/ora con uno dei seguenti formati:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* è compreso tra 0 e 23.

*`zzz`* è un codice del fuso orario di 3 o 4 caratteri, ad esempio  `GMT` o  `PST`. Il tempo di risparmio giornaliero deve essere contabilizzato nel codice del fuso orario (ad esempio `PST` per l&#39;ora standard del Pacifico, rispetto a `PDT` per l&#39;ora legale del Pacifico).

*`offset`* è un offset del fuso orario espresso in ore o ore:minuti, rispetto al valore GMT. Ad esempio, `PDT` equivale a `GMT -7`.

Devono essere presenti tutti gli elementi dei valori data/ora formattati in stringa. Se il valore data/ora non è formattato correttamente, viene ignorato e viene utilizzata l&#39;ora di modifica del file [!DNL *`catalog`*.ini].

## Predefinito {#section-ac465313c97943ed97d41ea852329177}

Se vuoto o non definito, il server utilizza il tempo di modifica del file ` *`catalog`*.ini`.

## Consultate anche {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [attributo::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attributo::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
