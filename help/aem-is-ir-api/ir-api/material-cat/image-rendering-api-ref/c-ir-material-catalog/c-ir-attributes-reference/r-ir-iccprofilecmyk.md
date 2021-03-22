---
description: Spazio colore predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigi quando con icc= non è specificato alcuno spazio colore di output.
seo-description: Spazio colore predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigi quando con icc= non è specificato alcuno spazio colore di output.
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
uuid: d923d0fd-f00b-4fce-8ce9-8b177b4dba96
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---


# IccProfileCmyk{#iccprofilecmyk}

Spazio colore predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigi quando con icc= non è specificato alcuno spazio colore di output.

## Proprietà {#section-849678b272954bdcb236f49aa54f1609}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido dalla mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo CMYK.

## Predefinito {#section-55026b7454af4d868bcb47f7743c9c5b}

Ereditato da `default::IccProfileCmyk` se non definito o se vuoto.

## Consultate anche {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attributo::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2),  [attributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
