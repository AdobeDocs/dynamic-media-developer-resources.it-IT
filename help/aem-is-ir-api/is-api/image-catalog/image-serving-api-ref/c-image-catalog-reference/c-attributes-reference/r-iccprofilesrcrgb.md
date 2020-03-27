---
description: Profilo colore di input predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente RGB che non incorporano un profilo colore e per alcuni valori di colore RGB specificati con vari comandi Image Server, ad esempio color=.
seo-description: Profilo colore di input predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente RGB che non incorporano un profilo colore e per alcuni valori di colore RGB specificati con vari comandi Image Server, ad esempio color=.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

Profilo colore di input predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente RGB che non incorporano un profilo colore e per alcuni valori di colore RGB specificati con vari comandi Image Server, ad esempio color=.

## Proprietà {#section-3cd753196959462e9e674dab0b033d08}

Stringa di testo. Se specificato, deve essere un `icc::Name` valore valido dalla mappa profilo ICC di questo catalogo immagini o del catalogo predefinito, oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo RGB.

## Predefinito {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Ereditato da `default::IccProfileSrcRgb` se non definito o se vuoto. Se `attribute::IccProfileSrcRgb` non si risolve in un profilo valido, `attribute::IccProfileRgb` viene utilizzato al posto.

## Consultate anche {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
