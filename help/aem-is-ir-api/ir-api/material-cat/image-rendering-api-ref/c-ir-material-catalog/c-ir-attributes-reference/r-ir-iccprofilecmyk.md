---
title: IccProfileCmyk
description: Spazio colore predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigio quando non è specificato alcuno spazio colore di output con icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c36ea45d-dc91-4afa-825a-7af49738101c
TQID: 'https://experienceleague.adobe.com/EjbyUNxki4CNWJFUr-9QI8ygzLldCWO54HxN-7SE8dM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

Spazio colore predefinito CMYK. Specifica il nome del profilo colore ICC da utilizzare per le immagini di risposta in scala di grigio quando non è specificato alcuno spazio colore di output con `icc=`.

## Proprietà {#section-849678b272954bdcb236f49aa54f1609}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido della mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo CMYK.

## Predefinito {#section-55026b7454af4d868bcb47f7743c9c5b}

Ereditato da `default::IccProfileCmyk` se non definito o se vuoto.

## Consultate anche {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
