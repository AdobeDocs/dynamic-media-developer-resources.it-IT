---
title: Timestamp
description: Timestamp di modifica del file. Specifica la data/ora dell'ultima modifica apportata all'immagine e/o ai file di dati allegati al record catalogo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 1%

---

# Timestamp{#timestamp}

Timestamp di modifica del file. Specifica la data/ora dell&#39;ultima modifica apportata all&#39;immagine e/o ai file di dati allegati al record catalogo.

Se `attribute::UseLastModified` è impostato, il più recente dei `catalog::TimeStamp` e `vignette::TimeStamp` I valori di tutti i materiali e la vignettatura coinvolti nella richiesta vengono restituiti nella risposta HTTP come intestazione modificata per ultima.

>[!NOTE]
>
>Gli orari effettivi dei file immagine o dati allegati a questo record catalogo non vengono mai utilizzati a questo scopo.

Il `catalog::TimeStamp` viene utilizzato anche per la convalida della cache basata su catalogo (vedi [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Proprietà {#section-42f09e375e72492b87a3a486da7df808}

Valore data/ora in formato Java™. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, 1 gennaio 1970 UTC/GMT, o un valore stringa data/ora con uno dei seguenti formati:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* è compreso nell&#39;intervallo tra 0 e 23.
* *[!DNL zzz]* è un codice di fuso orario di tre o quattro caratteri, ad esempio &#39;GMT&#39; o &#39;PST&#39;. L’ora legale deve essere registrata nel codice del fuso orario. Ad esempio, &quot;PST&quot; per l’ora solare Pacifico rispetto a &quot;PDT&quot; per l’ora legale Pacifico.
* *[!DNL offset]* è uno scostamento del fuso orario in ore o ore:minuti, relativo a GMT. Ad esempio, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Tutti gli elementi dei valori di data/ora in formato stringa devono essere presenti. Se il valore data/ora non è formattato correttamente, viene ignorato e l’ora di modifica del *catalogo* Viene utilizzato il file .ini.

## Predefinito {#section-e2c126c9e7294662b23944ab8d14866b}

Il `attribute::TimeStamp` è il campo vuoto o non presente.

## Consultate anche {#section-876f1d1b50dc4501b605820015a29451}

[attribute::Timestamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignettatura::Timestamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
