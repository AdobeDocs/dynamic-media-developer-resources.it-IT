---
description: Profilo colore di uscita predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta RGB quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori colore RGB specificati con vari comandi Image Rendering, come bgc= e color=.
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# IccProfileRgb{#iccprofilergb}

Profilo colore di uscita predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta RGB quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori colore RGB specificati con vari comandi Image Rendering, come bgc= e color=.

## Proprietà {#section-b4a1bd92e99047479a5036413525a6d9}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa del profilo ICC di questo catalogo dei materiali o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo RGB.

## Predefinito {#section-5809772f8e96438ab7626d323c66a4ba}

Ereditato da `default::IccProfileRgb` se non definito o se vuoto.

## Consultate anche {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attributo::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49),  [attributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
