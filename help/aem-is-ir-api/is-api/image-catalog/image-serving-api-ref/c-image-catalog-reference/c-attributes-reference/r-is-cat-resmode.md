---
title: ResMode
description: Modalità di ricampionamento predefinita. Specifica gli attributi di ricampionamento e interpolazione predefiniti da utilizzare per il ridimensionamento dei dati immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# ResMode{#resmode}

Modalità di ricampionamento predefinita. Specifica gli attributi di ricampionamento e interpolazione predefiniti da utilizzare per il ridimensionamento dei dati immagine.

Utilizzato quando `resMode=` non è specificato in una richiesta.

## Proprietà {#section-493f900be522486f97710cebdc4460c2}

Enum. Imposta su 2 per `bilin`, 3 per `bicub`o 4 per `sharp2` modalità di interpolazione (vedere [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) per ulteriori informazioni). `sharp` (1) è stato dichiarato obsoleto. Utilizzo `sharp2` (4) invece per i migliori risultati.

## Predefinito {#section-35f980e745fc4d79a2621e8abacc724d}

Ereditato da `default::ResMode` se non definito o se vuoto.

## Consultate anche {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
