---
title: Timestamp
description: Timestamp di modifica predefinito. Fornisce un valore predefinito per la marca temporale e la marca temporale della vignettatura del catalogo. Se non viene specificato, il server utilizza la data/ora di modifica di questo file catalog.ini.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
TQID: 'https://experienceleague.adobe.com/p3g5NQf25sagtaAYjdd4Vd8J6kZBAoLM8tSY42NPuOI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 218
ht-degree: 1%

---

# Timestamp{#timestamp}

Timestamp di modifica predefinito. Fornisce un valore predefinito per `catalog::TimeStamp` e `vignette::TimeStamp`. Se non viene specificato, il server utilizza la data/ora di modifica di questo file catalog.ini.

## Proprietà {#section-910e2562b41c47b78ee6216deeabbbd5}

Valore data/ora in formato Java™. Può essere il numero intero di millisecondi trascorsi dalla mezzanotte, 1 gennaio 1970 UTC/GMT, o un valore stringa data/ora con uno dei seguenti formati:

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* è compreso tra 0 e 23.

*[!DNL zzz]* è un codice di fuso orario di tre o quattro caratteri come &#39;GMT&#39; o &#39;PST&#39;. L’ora legale deve essere inclusa nel codice del fuso orario (ad esempio, &quot;PST&quot; per l’ora solare Pacifico e &quot;PDT&quot; per l’ora legale Pacifico).

*[!DNL offset]* è una differenza di fuso orario in ore o ore:minutes, relativa a GMT. Ad esempio, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Tutti gli elementi dei valori di data/ora in formato stringa devono essere presenti. Se il valore data/ora non è formattato correttamente, viene ignorato e viene utilizzata l&#39;ora di modifica del file [!DNL *[!DNL catalog]*.ini].

## Predefinito {#section-65fb29a9ea2044df8cb9fe295eb14872}

Se vuoto o non definito, il server utilizza l&#39;ora di modifica del file [!DNL *[!DNL catalog]*.ini].

## Consultate anche {#section-764188f9b1734ad1a6270f5fecd28532}

[catalogo::Timestamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignettatura::Timestamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1), [attributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attributo::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
