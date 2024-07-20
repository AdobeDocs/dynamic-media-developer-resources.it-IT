---
description: Dimensioni immagine. Dimensione in pixel dell'immagine a risoluzione massima a cui fa riferimento il percorso del catalogo.
solution: Experience Manager
title: Dimensione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 5%

---

# Dimensione{#size}

Dimensioni immagine. Dimensione in pixel dell&#39;immagine a risoluzione massima a cui fa riferimento catalog::Path.

Se viene fornito questo valore, Image Server lo utilizza per evitare di dover aprire l&#39;immagine per ottenere le dimensioni effettive.

>[!NOTE]
>
>Se `catalog::Size` è fornito e non corrisponde alla dimensione immagine a risoluzione massima effettiva, potrebbe verificarsi un comportamento non definito.

## Proprietà {#section-5c914ec8b1444a8e99d811b647cd42a3}

Due numeri interi, ciascuno maggiore di 0, separati da una virgola. Facoltativo.

## Predefinito {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Se il campo non è presente o se il campo è vuoto, vengono utilizzate le dimensioni effettive dell’immagine.

## Consultate anche {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalogo::Percorso](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
