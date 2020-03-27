---
description: Dimensione immagine. Dimensione in pixel dell’immagine a risoluzione piena cui fa riferimento il percorso del catalogo.
seo-description: Dimensione immagine. Dimensione in pixel dell’immagine a risoluzione piena cui fa riferimento il percorso del catalogo.
seo-title: Dimensione
solution: Experience Manager
title: Dimensione
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Dimensione{#size}

Dimensione immagine. Dimensione in pixel dell’immagine a risoluzione piena a cui fa riferimento il catalogo::Path.

Se questo valore viene fornito, Image Server lo utilizza per evitare di dover aprire l’immagine per ottenere le dimensioni effettive.

>[!NOTE]
>
>Se `catalog::Size`viene fornito e non equivale alla dimensione effettiva dell’immagine a risoluzione piena, potrebbe verificarsi un comportamento non definito.

## Proprietà {#section-5c914ec8b1444a8e99d811b647cd42a3}

Due numeri interi, ciascuno maggiore di 0, separati da una virgola. Facoltativo.

## Predefinito {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Se il campo non è presente o se il campo è vuoto, viene utilizzata la dimensione effettiva dell&#39;immagine.

## Consultate anche {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalogo::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
