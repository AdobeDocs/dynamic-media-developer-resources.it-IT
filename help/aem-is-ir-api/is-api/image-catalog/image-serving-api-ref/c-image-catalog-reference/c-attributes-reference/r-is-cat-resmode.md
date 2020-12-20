---
description: Modalità di ricampionamento predefinita. Specifica gli attributi di ricampionamento e interpolazione predefiniti da usare per il ridimensionamento dei dati immagine.
seo-description: Modalità di ricampionamento predefinita. Specifica gli attributi di ricampionamento e interpolazione predefiniti da usare per il ridimensionamento dei dati immagine.
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 5%

---


# ResMode{#resmode}

Modalità di ricampionamento predefinita. Specifica gli attributi di ricampionamento e interpolazione predefiniti da usare per il ridimensionamento dei dati immagine.

Utilizzato quando `resMode=` non è specificato in una richiesta.

## Proprietà {#section-493f900be522486f97710cebdc4460c2}

Enum. Impostare su 2 per `bilin`, 3 per `bicub` o 4 per la modalità di interpolazione `sharp2` (vedere ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` per i dettagli). `sharp` (1) è stato dichiarato obsoleto. Utilizzate `sharp2` (4) invece per ottenere risultati ottimali.

## Predefinito {#section-35f980e745fc4d79a2621e8abacc724d}

Ereditato da `default::ResMode` se non definito o se vuoto.

## Consultate anche {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
