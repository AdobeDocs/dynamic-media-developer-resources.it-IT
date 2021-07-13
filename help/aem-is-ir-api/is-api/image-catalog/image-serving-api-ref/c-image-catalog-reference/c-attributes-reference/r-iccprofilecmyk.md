---
description: Profilo colore di output predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta CMYK quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori di colore CMYK specificati con vari comandi Image Serving, ad esempio color=.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

Profilo colore di output predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta CMYK quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori di colore CMYK specificati con vari comandi Image Serving, ad esempio color=.

## Proprietà {#section-d8b6102cc1c744d482f99808ccfcaa24}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo CMYK.

## Predefinito {#section-62442df09a724950bfbdd0640b3e6678}

Ereditato da `default::IccProfileCmyk` se non definito o se vuoto.

## Consultate anche {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attributo::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728),  [attributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
