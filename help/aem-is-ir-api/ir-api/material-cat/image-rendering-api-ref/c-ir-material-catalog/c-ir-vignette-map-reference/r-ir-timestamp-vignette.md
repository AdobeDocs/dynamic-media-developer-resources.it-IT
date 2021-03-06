---
description: Timestamp della modifica. Specifica la data/ora dell'ultima modifica apportata alla vignetta.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Timestamp della modifica. Specifica la data/ora dell&#39;ultima modifica apportata alla vignetta.

Se `attribute::UseLastModified` è impostato il più recente `vignette::TimeStamp` e `catalog::TimeStamp`il valore della vignetta e di tutti i materiali coinvolti nella richiesta viene restituito nella risposta HTTP come intestazione dell’ultima modifica.

>[!NOTE]
>
>A questo scopo non viene mai utilizzato il tempo effettivo del file di vignetta.

`catalog::TimeStamp` viene utilizzato anche per la convalida della cache basata su catalogo (vedi [attributo::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Proprietà {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valore data/ora in formato Java. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, dal 1° gennaio 1970 UTC/GMT o un valore di stringa data/ora con uno dei seguenti formati:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* è compreso tra 0 e 23.
* *[!DNL zzz]* è un codice del fuso orario a 3 o 4 caratteri come &quot;GMT&quot; o &quot;PST&quot;. L’ora legale deve essere contabilizzata nel codice del fuso orario (ad esempio, &quot;PST&quot; per l’ora standard del Pacifico, rispetto a &quot;PDT&quot; per l’ora legale del Pacifico).
* *[!DNL offset]* è un offset del fuso orario in ore o ore:minuti, relativo a GMT. Ad esempio, &quot;PDT&quot; equivale a &quot;GMT -7&quot;.

Tutti gli elementi dei valori data/ora formattati in stringa devono essere presenti. Se il valore data/ora non è formattato correttamente, viene ignorato e l’ora di modifica del [!DNL *[!DNL catalog]* Viene invece utilizzato il file .ini.

## Predefinito {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` è il campo è vuoto o non è presente.

## Consultate anche {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
