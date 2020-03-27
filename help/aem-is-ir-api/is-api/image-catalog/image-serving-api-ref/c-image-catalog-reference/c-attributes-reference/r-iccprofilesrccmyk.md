---
description: Profilo colore di input predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente CMYK che non incorporano un profilo colore e per alcuni valori di colore CMYK specificati con vari comandi Image Server, ad esempio color=.
seo-description: Profilo colore di input predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente CMYK che non incorporano un profilo colore e per alcuni valori di colore CMYK specificati con vari comandi Image Server, ad esempio color=.
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 5f1c2eb6-7f32-4603-9587-d8c1f6a72bb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

Profilo colore di input predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente CMYK che non incorporano un profilo colore e per alcuni valori di colore CMYK specificati con vari comandi Image Server, ad esempio color=.

## Proprietà {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Stringa di testo. Se specificato, deve essere un `icc::Name` valore valido dalla mappa profilo ICC di questo catalogo immagini o del catalogo predefinito, oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo CMYK.

## Predefinito {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Ereditato da `default::IccProfileSrcCmyk` se non definito o se vuoto. Se `attribute::IccProfileSrcCmyk` non si risolve in un profilo valido, `attribute::IccProfileCmyk` viene utilizzato al posto.

## Consultate anche {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
