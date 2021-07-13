---
description: Risoluzione. Risoluzione delle immagini "nel mondo reale", in genere espressa in pixel per pollice, ma anche in altre unità, come i pixel per metro.
solution: Experience Manager
title: Risoluzione
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 7%

---

# Risoluzione{#resolution}

Risoluzione. Risoluzione delle immagini &quot;nel mondo reale&quot;, in genere espressa in pixel per pollice, ma anche in altre unità, come i pixel per metro.

## Proprietà {#section-985ca2ad858c4e9c9cbb303f55447553}

Numero reale, maggiore di 0. Richiesto per i materiali di texture e decal, a meno che la risoluzione dell&#39;immagine non sia la stessa dell&#39;attributo::Resolution. Ignorato da colori solidi e materiali per armadietti.

## Predefinito {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` viene utilizzato se il campo non è presente, se il valore è 0 o negativo o se il campo è vuoto.

## Consultate anche {#section-2d04df523d7345f6929178cbc637da78}

[attributo::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) ,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
