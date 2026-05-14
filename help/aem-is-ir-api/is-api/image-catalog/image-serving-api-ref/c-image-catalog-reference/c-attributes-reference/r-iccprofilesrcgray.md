---
description: Profilo colore di input predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente in scala di grigio che non incorporano un profilo colore e per determinati valori di colore in scala di grigio specificati con vari comandi Image Server, ad esempio color=.
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54290f71-36b2-4b37-ac04-4fe85c1f34ab
TQID: 'https://experienceleague.adobe.com/T6hvJ0NuHHHN3io1u0BbkQMbaIZEPXpwZJddf-VR7So'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 1%

---

# IccProfileSrcGray{#iccprofilesrcgray}

Profilo colore di input predefinito in scala di grigio. Specifica il nome del profilo colore ICC da utilizzare per le immagini sorgente in scala di grigio che non incorporano un profilo colore e per determinati valori di colore in scala di grigio specificati con vari comandi Image Server, ad esempio color=.

## Proprietà {#section-8cbb316df6eb463aaca7b308d3568086}

Stringa di testo. Se specificato, deve essere un valore `icc::Name` valido della mappa del profilo ICC di questo catalogo immagini o del catalogo predefinito oppure un percorso di file relativo a `attribute::RootPath`. Il profilo ICC di riferimento deve essere un profilo in scala di grigio.

## Predefinito {#section-bcc7250715884412bd0780f60d1cce7b}

Ereditato da `default::IccProfileSrcGray` se non definito o se vuoto. Se `attribute::IccProfileSrcGray` non viene risolto in un profilo valido, viene utilizzato `attribute::IccProfileGray`.

## Consultate anche {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
