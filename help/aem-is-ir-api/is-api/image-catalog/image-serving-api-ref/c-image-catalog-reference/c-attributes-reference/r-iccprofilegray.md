---
description: Profilo colore di output predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigio quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori di colore in scala di grigio specificati con vari comandi Image Serving, ad esempio color=.
seo-description: Profilo colore di output predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigio quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori di colore in scala di grigio specificati con vari comandi Image Serving, ad esempio color=.
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
topic: Scene7 Image Serving - Image Rendering API
uuid: a7d40114-f91f-4637-bb49-5b06b9ce846d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileGray{#iccprofilegray}

Profilo colore di output predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigio quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori di colore in scala di grigio specificati con vari comandi Image Serving, ad esempio color=.

## Proprietà {#section-03f090ee2acf4537b83f78840d23ecab}

Stringa di testo. Se specificato, deve essere un `icc::Name` valore valido dalla mappa profilo ICC di questo catalogo immagini o del catalogo predefinito, oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo in scala di grigio.

## Predefinito {#section-95ba3ab15edc4259b657c6ebf8783d61}

Ereditato da `default::IccProfileGray` se non definito o se vuoto.

## Consultate anche {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
