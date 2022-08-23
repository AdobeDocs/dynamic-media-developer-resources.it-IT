---
title: IccProfileCmyk
description: Spazio colore predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigi quando con icc= non è specificato alcuno spazio colore di output.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c36ea45d-dc91-4afa-825a-7af49738101c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# IccProfileCmyk{#iccprofilecmyk}

Spazio colore predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigi quando non è specificato alcuno spazio colore di output con `icc=`.

## Proprietà {#section-849678b272954bdcb236f49aa54f1609}

Stringa di testo. Se specificato, deve essere valido `icc::Name` dalla mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito, o da un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo CMYK.

## Predefinito {#section-55026b7454af4d868bcb47f7743c9c5b}

Ereditato da `default::IccProfileCmyk` se non definito o se vuoto.

## Consultate anche {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attributo::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2), [attributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
