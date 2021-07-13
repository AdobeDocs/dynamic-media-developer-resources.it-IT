---
description: Profilo colore di input predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale CMYK che non incorporano un profilo colore.
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Profilo colore di input predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale CMYK che non incorporano un profilo colore.

## Proprietà {#section-0cee77438d914c319ec876edb3490821}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo CMYK.

## Predefinito {#section-11f6239e0dd14827abf4a95c1b30161c}

Ereditato da `default::IccProfileSrcCmyk` se non definito o se vuoto. Se `attribute::IccProfileSrcCmyk` non viene risolto in un profilo valido, verrà utilizzato `attribute::IccProfileCmyk`.

## Consultate anche {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attributo::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [attributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
