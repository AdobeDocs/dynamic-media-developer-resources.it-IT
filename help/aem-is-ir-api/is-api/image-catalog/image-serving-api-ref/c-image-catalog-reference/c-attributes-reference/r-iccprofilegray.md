---
description: Profilo colore di output predefinito in scala di grigi. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigi quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori di colore in scala di grigi specificati con vari comandi Image Serving, ad esempio color=.
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# IccProfileGray{#iccprofilegray}

Profilo colore di output predefinito in scala di grigi. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigi quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori di colore in scala di grigi specificati con vari comandi Image Serving, ad esempio color=.

## Proprietà {#section-03f090ee2acf4537b83f78840d23ecab}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo in scala di grigi.

## Predefinito {#section-95ba3ab15edc4259b657c6ebf8783d61}

Ereditato da `default::IccProfileGray` se non definito o se vuoto.

## Consultate anche {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attributo::IccProfileSrcGrey](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9),  [attributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
