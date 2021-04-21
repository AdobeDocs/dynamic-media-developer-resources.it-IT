---
description: Profilo colore di ingresso predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente RGB che non incorporano un profilo colore e per alcuni valori colore RGB specificati con vari comandi Image Serving, ad esempio color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

Profilo colore di ingresso predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente RGB che non incorporano un profilo colore e per alcuni valori colore RGB specificati con vari comandi Image Serving, ad esempio color=.

## Proprietà {#section-3cd753196959462e9e674dab0b033d08}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo RGB.

## Predefinito {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Ereditato da `default::IccProfileSrcRgb` se non definito o se vuoto. Se `attribute::IccProfileSrcRgb` non viene risolto in un profilo valido, viene invece utilizzato `attribute::IccProfileRgb`.

## Consultate anche {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attributo::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df),  [attributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
