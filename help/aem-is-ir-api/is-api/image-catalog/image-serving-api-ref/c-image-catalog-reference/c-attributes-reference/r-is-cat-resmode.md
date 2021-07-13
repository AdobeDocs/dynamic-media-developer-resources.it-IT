---
description: Modalità di ricampionamento predefinita. Specifica gli attributi di ricampionamento e interpolazione predefiniti da utilizzare per il ridimensionamento dei dati immagine.
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ResMode{#resmode}

Modalità di ricampionamento predefinita. Specifica gli attributi di ricampionamento e interpolazione predefiniti da utilizzare per il ridimensionamento dei dati immagine.

Utilizzato quando `resMode=` non è specificato in una richiesta.

## Proprietà {#section-493f900be522486f97710cebdc4460c2}

Enum. Impostare su 2 per `bilin`, 3 per `bicub` o 4 per la modalità di interpolazione `sharp2` (vedere ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` per i dettagli). `sharp` (1) è stato dichiarato obsoleto. Utilizza invece `sharp2` (4) per ottenere risultati migliori.

## Predefinito {#section-35f980e745fc4d79a2621e8abacc724d}

Ereditato da `default::ResMode` se non definito o se vuoto.

## Consultate anche {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
