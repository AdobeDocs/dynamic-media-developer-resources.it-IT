---
description: Timestamp di modifica immagine predefinito. Specifica un valore predefinito per il Timestamp del catalogo.
solution: Experience Manager
title: Timestamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---

# Timestamp{#timestamp}

Timestamp di modifica immagine predefinito. Specifica un valore predefinito per catalog::TimeStamp.

Se non viene specificato, il server utilizzerà la data/ora di modifica di questo [!DNL *`catalog`*.ini] file.

## Proprietà {#section-647066e62ce44a84b627fdd0b2f7cfec}

Valore data/ora. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, 1 gennaio 1970 UTC/GMT o un valore stringa data/ora con uno dei seguenti formati:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* è compreso tra 0 e 23.

*`zzz`* è un codice di fuso orario di 3 o 4 caratteri come `GMT` o `PST`. L’ora legale deve essere registrata nel codice del fuso orario (ad es. `PST` per l&#39;ora solare Pacifico, vs `PDT` per l&#39;ora legale del Pacifico).

*`offset`* è uno scostamento del fuso orario in ore o ore:minuti, relativo a GMT. Ad esempio: `PDT` equivale a `GMT -7`.

Tutti gli elementi dei valori di data/ora in formato stringa devono essere presenti. Se il valore data/ora non è formattato correttamente, viene ignorato e l’ora di modifica del [!DNL *`catalog`*.ini] al suo posto viene utilizzato il file.

## Predefinito {#section-ac465313c97943ed97d41ea852329177}

Se vuoto o non definito, il server utilizza l&#39;ora di modifica del file `*`catalogo`*.ini` file.

## Consultate anche {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalogo::Timestamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
