---
description: Profilo colore di ingresso predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini e le vignette del materiale RGB che non incorporano un profilo colore e per i valori di colore RGB specificati con vari comandi Image Rendering, come bgc= e color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

Profilo colore di ingresso predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini e le vignette del materiale RGB che non incorporano un profilo colore e per i valori di colore RGB specificati con vari comandi Image Rendering, come bgc= e color=.

## Proprietà {#section-c22966bba03e43c08e9d3fb91bfdd465}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo RGB.

## Predefinito {#section-0171cd6680284bfa9844b9cc3644ca61}

Ereditato da `default::IccProfileSrcRgb` se non definito o se vuoto. Se `attribute::IccProfileSrcRgb` non viene risolto in un profilo valido, viene invece utilizzato `attribute::IccProfileRgb`.

## Consultate anche {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attributo::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30),  [attributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
