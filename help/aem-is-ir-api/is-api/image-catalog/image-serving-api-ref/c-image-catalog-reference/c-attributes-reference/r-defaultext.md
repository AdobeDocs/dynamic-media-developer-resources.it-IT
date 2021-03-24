---
description: Suffisso predefinito del file immagine. Aggiunto al valore del campo Percorso catalogo (o MaskPath catalogo) se il percorso non include un suffisso di file
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# DefaultExt{#defaultext}

Suffisso predefinito del file immagine. Aggiunto al valore del campo catalogo::Path (o catalogo::MaskPath) se il percorso non include un suffisso di file

Un suffisso di file è costituito da un punto e da uno o più caratteri tra il punto e la fine della stringa. Il suffisso viene aggiunto al percorso http se il percorso non corrisponde a una voce di catalogo e se l&#39;ultimo elemento del percorso non include un suffisso di file.

## Proprietà {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Stringa di testo. Deve includere un &#39;&#39; iniziale. e uno o più caratteri.

## Predefinito {#section-1194c36ffe0748c5b9ff7d732a506588}

Ereditato da `default::DefaultExt` se non definito. Se definito ma vuoto, non viene applicato alcun suffisso predefinito ai nomi immagine quando si utilizza questo catalogo.

## Consultate anche {#section-d7c408b979844643adff8258f500eb7c}

[catalogo::Percorso](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catalogo::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
