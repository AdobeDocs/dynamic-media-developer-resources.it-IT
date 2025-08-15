---
title: Timestamp
description: Timestamp di modifica. Specifica la data/ora dell'ultima modifica apportata alla vignettatura.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# Timestamp{#timestamp}

Timestamp di modifica. Specifica la data/ora dell&#39;ultima modifica apportata alla vignettatura.

Se `attribute::UseLastModified` è impostato, il valore `vignette::TimeStamp` e `catalog::TimeStamp` più recente della vignettatura e di tutti i materiali coinvolti nella richiesta vengono restituiti nella risposta HTTP come intestazione dell&#39;ultima modifica.

>[!NOTE]
>
>L&#39;ora effettiva del file di vignettatura non viene mai utilizzata per questo scopo.

`catalog::TimeStamp` viene utilizzato anche per la convalida della cache basata su catalogo. Vedere [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Proprietà {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valore data/ora in formato Java™. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, 1 gennaio 1970 UTC/GMT, o un valore stringa data/ora con uno dei seguenti formati:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*&#x200B;GMT *[!DNL offset]*

* *[!DNL hh]* è compreso nell&#39;intervallo tra 0 e 23.
* *[!DNL zzz]* è un codice di fuso orario di tre o quattro caratteri come &#39;GMT&#39; o &#39;PST&#39;. L’ora legale deve essere inclusa nel codice del fuso orario (ad esempio, &quot;PST&quot; per l’ora solare Pacifico e &quot;PDT&quot; per l’ora legale Pacifico).
* *[!DNL offset]* è una differenza di fuso orario in ore o ore:minutes, relativa a GMT. Ad esempio, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Tutti gli elementi dei valori di data/ora in formato stringa devono essere presenti. Se il valore data/ora non è formattato correttamente, viene ignorato e viene utilizzata l&#39;ora di modifica del file [!DNL *[!DNL catalog]*.ini].

## Predefinito {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` è il campo vuoto o non presente.

## Consultate anche {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attributo::Timestamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalogo::Timestamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
