---
description: Dimensioni immagine. Dimensione in pixel dell'immagine a risoluzione massima a cui fa riferimento il percorso del catalogo.
solution: Experience Manager
title: Dimensione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
TQID: 'https://experienceleague.adobe.com/wS28XEIvINBBoYZSI-frpSbCikCyC5AhT6TyDgMsGFg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
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
