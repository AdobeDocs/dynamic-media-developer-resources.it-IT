---
description: Profilo colore di uscita predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta RGB quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori colore RGB specificati con vari comandi Image Serving, ad esempio color=.
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

Profilo colore di uscita predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta RGB quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori colore RGB specificati con vari comandi Image Serving, ad esempio color=.

## Proprietà {#section-3dd55c954d4d4ad4bb715ed7cee31025}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo RGB.

## Predefinito {#section-dfe08dd7b851453ca816623a4179955b}

Ereditato da `default::IccProfileRgb` se non definito o se vuoto.

## Consultate anche {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attributo::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2),  [attributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
