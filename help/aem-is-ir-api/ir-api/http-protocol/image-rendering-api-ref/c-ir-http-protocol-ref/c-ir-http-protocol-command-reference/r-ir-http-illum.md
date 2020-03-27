---
description: Selettore mappa di illuminazione. Specifica la mappa di illuminazione con cui deve essere eseguito il rendering di questo materiale.
seo-description: Selettore mappa di illuminazione. Specifica la mappa di illuminazione con cui deve essere eseguito il rendering di questo materiale.
seo-title: illum
solution: Experience Manager
title: illum
topic: Scene7 Image Serving - Image Rendering API
uuid: 16c7144f-7f16-47d1-8140-fd679e702660
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# illum{#illum}

Selettore mappa di illuminazione. Specifica la mappa di illuminazione con cui deve essere eseguito il rendering di questo materiale.

`illum=-1|0|1|2`

Se la mappa di illuminazione specificata non è disponibile nella vignettatura di destinazione, viene usata la mappa disponibile più vicina.

`illum=-1` specifica che la mappa di illuminazione viene selezionata automaticamente in base al `gloss=` valore.

## Proprietà {#section-aace8466566e4cf1a0c5a6c0167245c9}

Attributo materiale. Ignorato se la vignettatura non definisce più mappe di illuminazione.

## Predefinito {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Consultate anche {#section-9132e60381c64aa3a8ed1319690db55e}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
