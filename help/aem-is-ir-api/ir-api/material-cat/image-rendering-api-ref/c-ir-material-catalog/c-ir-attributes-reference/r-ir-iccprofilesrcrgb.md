---
title: IccProfileSrcRgb
description: Profilo colore di input predefinito di RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale RGB e le vignette che non incorporano un profilo colore. Anche per i valori di colore RGB specificati con vari comandi Image Rendering, come bgc= e color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

Profilo colore di input predefinito di RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini di materiale RGB e le vignette che non incorporano un profilo colore. Anche per i valori di colore RGB specificati con vari comandi Image Rendering, ad esempio `bgc=` e `color=`.

## Proprietà {#section-c22966bba03e43c08e9d3fb91bfdd465}

Stringa di testo. Se specificato, deve essere valido `icc::Name` dalla mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito, o da un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo RGB.

## Predefinito {#section-0171cd6680284bfa9844b9cc3644ca61}

Ereditato da `default::IccProfileSrcRgb` se non definito o se vuoto. Se `attribute::IccProfileSrcRgb` non risolve in un profilo valido, `attribute::IccProfileRgb` viene invece utilizzato.

## Consultate anche {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attributo::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [attributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
