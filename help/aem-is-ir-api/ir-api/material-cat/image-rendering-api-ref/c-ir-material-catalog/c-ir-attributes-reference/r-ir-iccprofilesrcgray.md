---
title: IccProfileSrcGray
description: Profilo colore di input predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale in scala di grigio che non incorporano un profilo colore.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# IccProfileSrcGray{#iccprofilesrcgray}

Profilo colore di input predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale in scala di grigio che non incorporano un profilo colore.

## Proprietà {#section-97923d8561b845309442d57d017d91a4}

Stringa di testo. Se specificato, deve essere un `icc::Name` valore dalla mappa del profilo ICC di questo catalogo immagini o di quello predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo in scala di grigio.

## Predefinito {#section-02c52805ee13483dba7878aeab51f889}

Ereditato da `default::IccProfileSrcGray` se non è definita o se è vuota. Se `attribute::IccProfileSrcGray` non viene risolto in un profilo valido, `attribute::IccProfileGray` viene utilizzato al suo posto.

## Consultate anche {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Nome](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
