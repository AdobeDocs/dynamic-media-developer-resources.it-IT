---
description: Profilo colore di input predefinito di RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente RGB che non incorporano un profilo colore e per alcuni valori di colore RGB specificati con vari comandi Image Server, ad esempio color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfcbd9fe-e696-46e3-abbf-497dc55fe855
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

Profilo colore di input predefinito di RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente RGB che non incorporano un profilo colore e per alcuni valori di colore RGB specificati con vari comandi Image Server, ad esempio color=.

## Proprietà {#section-3cd753196959462e9e674dab0b033d08}

Stringa di testo. Se specificato, deve essere un `icc::Name` valore dalla mappa del profilo ICC di questo catalogo immagini o di quello predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo RGB.

## Predefinito {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Ereditato da `default::IccProfileSrcRgb` se non è definita o se è vuota. Se `attribute::IccProfileSrcRgb` non viene risolto in un profilo valido, `attribute::IccProfileRgb` viene utilizzato al suo posto.

## Consultate anche {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Nome](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
