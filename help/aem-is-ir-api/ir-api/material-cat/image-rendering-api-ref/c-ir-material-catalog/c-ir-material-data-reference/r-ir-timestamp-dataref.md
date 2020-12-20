---
description: Timestamp modifica file. Specifica la data/ora dell'ultima modifica apportata ai file di immagine e/o dati allegati al record del catalogo.
seo-description: Timestamp modifica file. Specifica la data/ora dell'ultima modifica apportata ai file di immagine e/o dati allegati al record del catalogo.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 77ce8bee-7b55-4ff8-8dfb-ebd3ce9c7a8a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# TimeStamp{#timestamp}

Timestamp modifica file. Specifica la data/ora dell&#39;ultima modifica apportata ai file di immagine e/o dati allegati al record del catalogo.

Se è impostata `attribute::UseLastModified`, la risposta HTTP più recente dei valori `catalog::TimeStamp` e `vignette::TimeStamp` di tutti i materiali e la vignettatura interessata dalla richiesta viene restituita come ultima intestazione modificata nella risposta HTTP.

>[!NOTE]
>
>A questo scopo non vengono mai utilizzati i tempi effettivi dei file immagine o dei file di dati allegati al record del catalogo.

`catalog::TimeStamp` viene utilizzata anche per la convalida della cache basata su catalogo (vedere  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Proprietà {#section-42f09e375e72492b87a3a486da7df808}

Valore data/ora in formato Java. Può essere il numero intero di millisecondi trascorsi a partire da mezzanotte, il 1 gennaio 1970 UTC/GMT oppure un valore di stringa data/ora con uno dei seguenti formati:

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

* *[!DNL hh]* è compreso tra 0 e 23.
* *[!DNL zzz]* è un codice del fuso orario di 3 o 4 caratteri, ad esempio &#39;GMT&#39; o &#39;PST&#39;. L&#39;ora legale deve essere contabilizzata nel codice del fuso orario (ad esempio, &#39;PST&#39; per l&#39;ora standard del Pacifico, invece di &#39;PDT&#39; per l&#39;ora legale del Pacifico).
* *[!DNL offset]* è un offset del fuso orario espresso in ore o ore:minuti, rispetto al valore GMT. Ad esempio, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Devono essere presenti tutti gli elementi dei valori data/ora formattati in stringa. Se il valore data/ora non è formattato correttamente, viene ignorato e viene utilizzata l&#39;ora di modifica del file *catalog*.ini.

## Predefinito {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` è il campo vuoto o non presente.

## Consultate anche {#section-876f1d1b50dc4501b605820015a29451}

[attributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [attributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [attributo::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4),  [vignettatura::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
