---
title: IccProfileRgb
description: Profilo colore di output predefinito di RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta RGB quando non è specificato alcuno spazio colore di output con icc=. Anche per alcuni valori di colore RGB specificati con vari comandi Image Rendering, come bgc= e color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
TQID: 'https://experienceleague.adobe.com/dyjS9FzJYrC4VXHr2olLvTUEXj-fjKwC1lIkCDc5D2E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

Profilo colore di output predefinito di RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta RGB quando non è specificato alcuno spazio colore di output con `icc=`. Anche per alcuni valori di colore RGB specificati con vari comandi Image Rendering, ad esempio `bgc=` e `color=`.

## Proprietà {#section-b4a1bd92e99047479a5036413525a6d9}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido della mappa del profilo ICC di questo catalogo dei materiali o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo RGB.

## Predefinito {#section-5809772f8e96438ab7626d323c66a4ba}

Ereditato da `default::IccProfileRgb` se non definito o se vuoto.

## Consultate anche {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
