---
description: URL principale per gli URL immagine relativi. Specifica l'URL principale per gli URL immagine relativi.
solution: Experience Manager
title: RootUrl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72560180-53e5-4293-9dd3-c0cd196551dc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---

# RootUrl{#rooturl}

URL principale per gli URL immagine relativi. Specifica l&#39;URL principale per gli URL immagine relativi.

`attribute::RootUrl` viene utilizzato al posto di `attribute::RootPath` quando un valore `src=` o `mask=` è racchiuso tra {parentesi graffe} o (parentesi graffe).

## Proprietà {#section-fe02269b4b724319a5d1f2cfcae31cba}

Valore stringa di testo. Percorso directory principale URL assoluto, incluso l’identificatore del protocollo principale. Sono supportati i seguenti protocolli: HTTP, HTTPS e FTP.

## Predefinito {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

Ereditato da `default::RootUrl` se non definito. Se definiti ma vuoti, gli URL relativi non sono supportati da questo catalogo immagini.

## Consultate anche {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [set di regole::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
