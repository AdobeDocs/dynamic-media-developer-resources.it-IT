---
description: Timestamp modifica. Specifica la data/ora dell'ultima modifica apportata alla vignettatura.
seo-description: Timestamp modifica. Specifica la data/ora dell'ultima modifica apportata alla vignettatura.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d2649e86-8a6f-4f63-ab6a-8b2d8c03f8c0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# TimeStamp{#timestamp}

Timestamp modifica. Specifica la data/ora dell&#39;ultima modifica apportata alla vignettatura.

Se è impostato `attribute::UseLastModified`, il valore più recente `vignette::TimeStamp` e `catalog::TimeStamp`della vignettatura e di tutti i materiali coinvolti nella richiesta viene restituito nella risposta HTTP come ultima intestazione modificata.

>[!NOTE]
>
>A questo scopo, la durata effettiva del file di vignettatura non viene mai utilizzata.

`catalog::TimeStamp` viene utilizzata anche per la convalida della cache basata su catalogo (vedere  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Proprietà {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valore data/ora in formato Java. Può essere il numero intero di millisecondi trascorsi a partire da mezzanotte, il 1 gennaio 1970 UTC/GMT oppure un valore di stringa data/ora con uno dei seguenti formati:

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*: *[!DNL ss]*GMT  *[!DNL offset]*

* *[!DNL hh]* è compreso tra 0 e 23.
* *[!DNL zzz]* è un codice del fuso orario di 3 o 4 caratteri, ad esempio &#39;GMT&#39; o &#39;PST&#39;. L&#39;ora legale deve essere contabilizzata nel codice del fuso orario (ad esempio, &#39;PST&#39; per l&#39;ora standard del Pacifico, invece di &#39;PDT&#39; per l&#39;ora legale del Pacifico).
* *[!DNL offset]* è un offset del fuso orario espresso in ore o ore:minuti, rispetto al valore GMT. Ad esempio, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Devono essere presenti tutti gli elementi dei valori data/ora formattati in stringa. Se il valore data/ora non è formattato correttamente, viene ignorato e viene utilizzata l&#39;ora di modifica del file [!DNL *[!DNL catalog]*.ini].

## Predefinito {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` è il campo vuoto o non presente.

## Consultate anche {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [catalogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319),  [attributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
