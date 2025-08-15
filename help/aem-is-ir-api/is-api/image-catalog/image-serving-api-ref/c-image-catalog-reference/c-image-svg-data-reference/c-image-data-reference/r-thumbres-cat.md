---
description: Risoluzione miniature. Specifica la risoluzione dell'oggetto per l'immagine miniatura.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

---

# ThumbRes{#thumbres}

Risoluzione miniature. Specifica la risoluzione dell&#39;oggetto per l&#39;immagine miniatura.

Utilizzato solo se `catalog::ThumbType=3`.

## Proprietà {#section-ee5cae086a3d4875805fa8a08756a586}

Valore numerico reale maggiore di 0. Deve avere le stesse unità di `catalog::Resolution`.

## Predefinito {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` viene utilizzato se il campo non è presente, se il valore è 0 o se il campo è vuoto.

## Consultate anche {#section-eb716bf647614db083020fe8ce453751}

[catalogo:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) , [catalog::Risoluzione](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [attributo::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Ridimensionamento miniature](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
