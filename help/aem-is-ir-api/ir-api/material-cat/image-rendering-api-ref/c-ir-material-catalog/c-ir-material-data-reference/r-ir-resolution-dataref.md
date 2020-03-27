---
description: Risoluzione. Risoluzione delle immagini "Real-world", solitamente espressa in pixel per pollice, ma anche in altre unità, come i pixel per metro.
seo-description: Risoluzione. Risoluzione delle immagini "Real-world", solitamente espressa in pixel per pollice, ma anche in altre unità, come i pixel per metro.
seo-title: Risoluzione
solution: Experience Manager
title: Risoluzione
topic: Scene7 Image Serving - Image Rendering API
uuid: 281c7ff6-8f78-4654-98ec-0db4299b80d9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Risoluzione{#resolution}

Risoluzione. Risoluzione delle immagini &quot;Real-world&quot;, solitamente espressa in pixel per pollice, ma anche in altre unità, come i pixel per metro.

## Proprietà {#section-985ca2ad858c4e9c9cbb303f55447553}

Numero reale, maggiore di 0. Richiesto per i materiali texture e decal, a meno che la risoluzione dell&#39;immagine non sia uguale all&#39;attributo::Resolution. Ignorata dai materiali in tinta unita e cabinet.

## Predefinito {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` viene utilizzato se il campo non è presente, se il valore è 0 o negativo o se il campo è vuoto.

## Consultate anche {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) , [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
