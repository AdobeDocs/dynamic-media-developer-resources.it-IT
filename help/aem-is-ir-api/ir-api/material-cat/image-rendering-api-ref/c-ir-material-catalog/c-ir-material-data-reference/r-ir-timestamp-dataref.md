---
description: Timestamp modifica file. Specifica la data/ora dell'ultima modifica apportata ai file di immagine e/o dati allegati al record del catalogo.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Timestamp modifica file. Specifica la data/ora dell&#39;ultima modifica apportata ai file di immagine e/o dati allegati al record del catalogo.

Se `attribute::UseLastModified` è impostato, il più recente tra `catalog::TimeStamp` e `vignette::TimeStamp` i valori di tutti i materiali e la vignetta coinvolta nella richiesta vengono restituiti nella risposta HTTP come intestazione dell’ultima modifica.

>[!NOTE]
>
>A questo scopo non vengono mai utilizzati gli orari effettivi dei file di immagine o di dati allegati a questo record del catalogo.

`catalog::TimeStamp` viene utilizzato anche per la convalida della cache basata su catalogo (vedi [attributo::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Proprietà {#section-42f09e375e72492b87a3a486da7df808}

Valore data/ora in formato Java. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, dal 1° gennaio 1970 UTC/GMT o un valore di stringa data/ora con uno dei seguenti formati:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* è compreso tra 0 e 23.
* *[!DNL zzz]* è un codice del fuso orario a 3 o 4 caratteri come &quot;GMT&quot; o &quot;PST&quot;. L’ora legale deve essere contabilizzata nel codice del fuso orario (ad esempio, &quot;PST&quot; per l’ora standard del Pacifico, rispetto a &quot;PDT&quot; per l’ora legale del Pacifico).
* *[!DNL offset]* è un offset del fuso orario in ore o ore:minuti, relativo a GMT. Ad esempio, &quot;PDT&quot; equivale a &quot;GMT -7&quot;.

Tutti gli elementi dei valori data/ora formattati in stringa devono essere presenti. Se il valore data/ora non è formattato correttamente, viene ignorato e l’ora di modifica del *catalogo* Viene invece utilizzato il file .ini.

## Predefinito {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` è il campo è vuoto o non è presente.

## Consultate anche {#section-876f1d1b50dc4501b605820015a29451}

[attributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attributo::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignetta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
