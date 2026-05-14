---
description: Profilo colore di input predefinito di RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente RGB che non incorporano un profilo colore e per alcuni valori di colore RGB specificati con vari comandi Image Server, ad esempio color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfcbd9fe-e696-46e3-abbf-497dc55fe855
TQID: 'https://experienceleague.adobe.com/CPYMKHgIu7mllwz1C-EM190nZxHzJ3547TWIEevP1rc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

Profilo colore di input predefinito di RGB. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente RGB che non incorporano un profilo colore e per alcuni valori di colore RGB specificati con vari comandi Image Server, ad esempio color=.

## Proprietà {#section-3cd753196959462e9e674dab0b033d08}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido della mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo RGB.

## Predefinito {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Ereditato da `default::IccProfileSrcRgb` se non definito o se vuoto. Se `attribute::IccProfileSrcRgb` non viene risolto in un profilo valido, viene utilizzato `attribute::IccProfileRgb`.

## Consultate anche {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
