---
title: Timestamp
description: Timestamp di modifica immagine predefinito. Fornisce un valore predefinito per la marca temporale del catalogo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# Timestamp{#timestamp}

Timestamp di modifica immagine predefinito. Specifica un valore predefinito per catalog::TimeStamp.

Se non specificato, il server utilizza la data/ora di modifica di questo file [!DNL *`catalog`*.ini].

## Proprietà {#section-647066e62ce44a84b627fdd0b2f7cfec}

Valore data/ora. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, 1 gennaio 1970 UTC/GMT, o un valore stringa data/ora con uno dei seguenti formati:

Valore data/ora *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

Valore data/ora *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

Il valore di ora *`hh`* è compreso nell&#39;intervallo tra 0 e 23.

Il valore di ora *`zzz`* è un codice di fuso orario di tre o quattro caratteri, ad esempio `GMT` o `PST`. L&#39;ora legale deve essere considerata nel codice del fuso orario (ad esempio, `PST` per l&#39;ora solare Pacifico rispetto a `PDT` per l&#39;ora legale Pacifico).

Il valore di ora *`offset`* è uno scostamento del fuso orario espresso in ore o ore:minuti, relativo a GMT. `PDT`, ad esempio, equivale a `GMT -7`.

Tutti gli elementi dei valori di data/ora in formato stringa devono essere presenti. Se il valore data/ora non è formattato correttamente, viene ignorato e viene utilizzata l&#39;ora di modifica del file [!DNL *`catalog`*.ini].

## Predefinito {#section-ac465313c97943ed97d41ea852329177}

Se vuoto o non definito, il server utilizza l&#39;ora di modifica del file `*`catalog`*.ini`.

## Consultate anche {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalogo::Timestamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attributo::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attributo::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
