---
description: Timestamp di modifica predefinito. Fornisce un valore predefinito per TimeStamp e TimeStamp del catalogo. Se non viene specificato, il server utilizzerà la data/ora di modifica del file catalog.ini.
seo-description: Timestamp di modifica predefinito. Fornisce un valore predefinito per TimeStamp e TimeStamp del catalogo. Se non viene specificato, il server utilizzerà la data/ora di modifica del file catalog.ini.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
uuid: 10ceb600-1ed9-46a1-ae07-889d601ac0f4
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# TimeStamp{#timestamp}

Timestamp di modifica predefinito. Fornisce un valore predefinito per catalog::TimeStamp e vignette::TimeStamp. Se non viene specificato, il server utilizzerà la data/ora di modifica del file catalog.ini.

## Proprietà {#section-910e2562b41c47b78ee6216deeabbbd5}

Valore data/ora in formato Java. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, dal 1° gennaio 1970 UTC/GMT o un valore di stringa data/ora con uno dei seguenti formati:

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

*[!DNL hh]* è compreso tra 0 e 23.

*[!DNL zzz]* è un codice del fuso orario a 3 o 4 caratteri come &quot;GMT&quot; o &quot;PST&quot;. L’ora legale deve essere contabilizzata nel codice del fuso orario (ad esempio, &quot;PST&quot; per l’ora standard del Pacifico, rispetto a &quot;PDT&quot; per l’ora legale del Pacifico).

*[!DNL offset]* è un offset del fuso orario in ore o ore:minuti, relativo a GMT. Ad esempio, &quot;PDT&quot; equivale a &quot;GMT -7&quot;.

Tutti gli elementi dei valori data/ora formattati in stringa devono essere presenti. Se il valore data/ora non viene formattato correttamente, viene ignorato e viene invece utilizzata l’ora di modifica del file [!DNL *[!DNL catalog]*.ini].

## Predefinito {#section-65fb29a9ea2044df8cb9fe295eb14872}

Se il file è vuoto o non è definito, il server utilizzerà l’ora di modifica del file *[!DNL catalog]*.ini].

## Consultate anche {#section-764188f9b1734ad1a6270f5fecd28532}

[catalogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vignetta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1),  [attributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [attributo::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
