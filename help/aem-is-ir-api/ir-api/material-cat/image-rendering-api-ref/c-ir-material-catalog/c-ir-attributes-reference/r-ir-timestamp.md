---
description: Timestamp di modifica predefinito. Fornisce un valore predefinito per TimeStamp e TimeStamp del catalogo. Se non viene specificato, il server utilizzerà la data/ora di modifica del file catalog.ini.
seo-description: Timestamp di modifica predefinito. Fornisce un valore predefinito per TimeStamp e TimeStamp del catalogo. Se non viene specificato, il server utilizzerà la data/ora di modifica del file catalog.ini.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ceb600-1ed9-46a1-ae07-889d601ac0f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# TimeStamp{#timestamp}

Timestamp di modifica predefinito. Fornisce un valore predefinito per catalog::TimeStamp e vignettatura::TimeStamp. Se non viene specificato, il server utilizzerà la data/ora di modifica del file catalog.ini.

## Proprietà {#section-910e2562b41c47b78ee6216deeabbbd5}

Valore data/ora in formato Java. Può essere il numero intero di millisecondi trascorsi a partire da mezzanotte, il 1 gennaio 1970 UTC/GMT oppure un valore di stringa data/ora con uno dei seguenti formati:

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

*[!DNL hh]* è compreso tra 0 e 23.

*[!DNL zzz]* è un codice del fuso orario di 3 o 4 caratteri, ad esempio &#39;GMT&#39; o &#39;PST&#39;. L&#39;ora legale deve essere contabilizzata nel codice del fuso orario (ad esempio, &#39;PST&#39; per l&#39;ora standard del Pacifico, invece di &#39;PDT&#39; per l&#39;ora legale del Pacifico).

*[!DNL offset]* è un offset del fuso orario espresso in ore o ore:minuti, rispetto al valore GMT. Ad esempio, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Devono essere presenti tutti gli elementi dei valori data/ora formattati in stringa. Se il valore data/ora non è formattato correttamente, viene ignorato e viene utilizzata l&#39;ora di modifica del file [!DNL *[!DNL catalog]*.ini].

## Predefinito {#section-65fb29a9ea2044df8cb9fe295eb14872}

Se vuoto o non definito, il server utilizzerà l&#39;ora di modifica del file [!DNL *[!DNL catalog]*.ini] del file.

## Consultate anche {#section-764188f9b1734ad1a6270f5fecd28532}

[catalogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vignettatura::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1),  [attributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [attributo::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
