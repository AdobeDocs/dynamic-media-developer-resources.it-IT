---
description: Dimensione immagine. Dimensione in pixel dell’immagine a risoluzione piena cui fa riferimento il percorso del catalogo.
seo-description: Dimensione immagine. Dimensione in pixel dell’immagine a risoluzione piena cui fa riferimento il percorso del catalogo.
seo-title: Dimensione
solution: Experience Manager
title: Dimensione
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 11%

---


# Dimensione{#size}

Dimensione immagine. Dimensione in pixel dell’immagine a risoluzione piena a cui fa riferimento il catalogo::Path.

Se questo valore viene fornito, Image Server lo utilizza per evitare di dover aprire l’immagine per ottenere le dimensioni effettive.

>[!NOTE]
>
>Se `catalog::Size`è fornito e non è uguale alla dimensione effettiva dell&#39;immagine a piena risoluzione, potrebbe verificarsi un comportamento non definito.

## Proprietà {#section-5c914ec8b1444a8e99d811b647cd42a3}

Due numeri interi, ciascuno maggiore di 0, separati da una virgola. Facoltativo.

## Predefinito {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Se il campo non è presente o se il campo è vuoto, viene utilizzata la dimensione effettiva dell&#39;immagine.

## Consultate anche {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalogo::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) ,  [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
