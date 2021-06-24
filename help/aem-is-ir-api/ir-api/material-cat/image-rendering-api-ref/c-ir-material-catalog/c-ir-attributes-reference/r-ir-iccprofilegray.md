---
description: Spazio colore predefinito in scala di grigi. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigi quando con icc= non è specificato alcuno spazio colore di output.
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# IccProfileGray{#iccprofilegray}

Spazio colore predefinito in scala di grigi. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigi quando con icc= non è specificato alcuno spazio colore di output.

## Proprietà {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa del profilo ICC di questo catalogo dei materiali o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo in scala di grigi.

## Predefinito {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

Ereditato da `default::IccProfileGray` se non definito o se vuoto.

## Consultate anche {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attributo::IccProfileSrcGrey](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2),  [attributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
