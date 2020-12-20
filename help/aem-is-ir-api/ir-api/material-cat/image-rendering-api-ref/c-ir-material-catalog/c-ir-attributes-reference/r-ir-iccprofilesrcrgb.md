---
description: Profilo colore di input predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale RGB e le vignettature che non incorporano un profilo colore e per i valori di colore RGB specificati con vari comandi Image Rendering, come bgc= e color=.
seo-description: Profilo colore di input predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale RGB e le vignettature che non incorporano un profilo colore e per i valori di colore RGB specificati con vari comandi Image Rendering, come bgc= e color=.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 9657e296-0d2a-4b05-9be7-5a54d3277f90
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

Profilo colore di input predefinito RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale RGB e le vignettature che non incorporano un profilo colore e per i valori di colore RGB specificati con vari comandi Image Rendering, come bgc= e color=.

## Proprietà {#section-c22966bba03e43c08e9d3fb91bfdd465}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa profilo ICC di questo catalogo immagini o del catalogo predefinito, oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo RGB.

## Predefinito {#section-0171cd6680284bfa9844b9cc3644ca61}

Ereditato da `default::IccProfileSrcRgb` se non definito o se vuoto. Se `attribute::IccProfileSrcRgb` non viene risolto in un profilo valido, viene utilizzato `attribute::IccProfileRgb`.

## Consultate anche {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
