---
title: IccProfileSrcCmyk
description: Profilo colore di input predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente CMYK che non incorporano un profilo colore e per alcuni valori di colore CMYK specificati con vari comandi Image Server, ad esempio color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Profilo colore di input predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente CMYK che non incorporano un profilo colore e per alcuni valori di colore CMYK specificati con vari comandi Image Server, ad esempio color=.

## Proprietà {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido della mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo CMYK.

## Predefinito {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Ereditato da `default::IccProfileSrcCmyk` se non definito o se vuoto. Se `attribute::IccProfileSrcCmyk` non viene risolto in un profilo valido, viene utilizzato `attribute::IccProfileCmyk`.

## Consultate anche {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
