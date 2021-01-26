---
description: Profilo colore di input predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente in scala di grigio che non incorporano un profilo colore e per alcuni valori di colore in scala di grigio specificati con vari comandi Image Serving, ad esempio color=.
seo-description: Profilo colore di input predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente in scala di grigio che non incorporano un profilo colore e per alcuni valori di colore in scala di grigio specificati con vari comandi Image Serving, ad esempio color=.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# IccProfileSrcGray{#iccprofilesrcgray}

Profilo colore di input predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente in scala di grigio che non incorporano un profilo colore e per alcuni valori di colore in scala di grigio specificati con vari comandi Image Serving, ad esempio color=.

## Proprietà {#section-8cbb316df6eb463aaca7b308d3568086}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa profilo ICC di questo catalogo immagini o del catalogo predefinito, oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo in scala di grigio.

## Predefinito {#section-bcc7250715884412bd0780f60d1cce7b}

Ereditato da `default::IccProfileSrcGray` se non definito o se vuoto. Se `attribute::IccProfileSrcGray` non viene risolto in un profilo valido, viene utilizzato `attribute::IccProfileGray`.

## Consultate anche {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
