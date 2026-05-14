---
description: Profilo colore di output predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta CMYK quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori colore CMYK specificati con vari comandi Image Server, ad esempio color=.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
TQID: 'https://experienceleague.adobe.com/G0UbfC77naL9ki0QEcpEYCX5Z4Tr3wt7YL2bQi8ZNEI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

Profilo colore di output predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta CMYK quando non è specificato alcuno spazio colore di output con icc= e per alcuni valori colore CMYK specificati con vari comandi Image Server, ad esempio color=.

## Proprietà {#section-d8b6102cc1c744d482f99808ccfcaa24}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido della mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo CMYK.

## Predefinito {#section-62442df09a724950bfbdd0640b3e6678}

Ereditato da `default::IccProfileCmyk` se non definito o se vuoto.

## Consultate anche {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
