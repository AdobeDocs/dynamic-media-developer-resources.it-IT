---
description: Profilo colore di input predefinito in scala di grigi. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente in scala di grigi che non incorporano un profilo colore e per alcuni valori di colore in scala di grigi specificati con vari comandi Image Serving, ad esempio color=.
seo-description: Profilo colore di input predefinito in scala di grigi. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente in scala di grigi che non incorporano un profilo colore e per alcuni valori di colore in scala di grigi specificati con vari comandi Image Serving, ad esempio color=.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# IccProfileSrcGray{#iccprofilesrcgray}

Profilo colore di input predefinito in scala di grigi. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente in scala di grigi che non incorporano un profilo colore e per alcuni valori di colore in scala di grigi specificati con vari comandi Image Serving, ad esempio color=.

## Proprietà {#section-8cbb316df6eb463aaca7b308d3568086}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo in scala di grigi.

## Predefinito {#section-bcc7250715884412bd0780f60d1cce7b}

Ereditato da `default::IccProfileSrcGray` se non definito o se vuoto. Se `attribute::IccProfileSrcGray` non viene risolto in un profilo valido, viene invece utilizzato `attribute::IccProfileGray`.

## Consultate anche {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attributo::IccProfileGrey](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35),  [attributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
