---
description: Profilo colore di input predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale in scala di grigio che non incorporano un profilo colore.
seo-description: Profilo colore di input predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale in scala di grigio che non incorporano un profilo colore.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: e05d1185-ffd6-4c04-a2b8-52228beae37d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# IccProfileSrcGray{#iccprofilesrcgray}

Profilo colore di input predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale in scala di grigio che non incorporano un profilo colore.

## Proprietà {#section-97923d8561b845309442d57d017d91a4}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa profilo ICC di questo catalogo immagini o del catalogo predefinito, oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo in scala di grigio.

## Predefinito {#section-02c52805ee13483dba7878aeab51f889}

Ereditato da `default::IccProfileSrcGray` se non definito o se vuoto. Se `attribute::IccProfileSrcGray` non viene risolto in un profilo valido, verrà utilizzato `attribute::IccProfileGray`.

## Consultate anche {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
