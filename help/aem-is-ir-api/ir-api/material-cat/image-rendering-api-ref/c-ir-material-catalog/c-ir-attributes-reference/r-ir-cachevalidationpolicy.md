---
description: Criterio di convalida della cache del server. Specifica quando le voci della cache lato server vengono convalidate.
seo-description: Criterio di convalida della cache del server. Specifica quando le voci della cache lato server vengono convalidate.
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Scene7 Image Serving - Image Rendering API
uuid: 299dd5fe-9a0c-43df-a4c8-6b9e9c24003b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CacheValidationPolicy{#cachevalidationpolicy}

Criterio di convalida della cache del server. Specifica quando le voci della cache lato server vengono convalidate.

Con la convalida basata sulla scadenza, i materiali di origine e le vignettature vengono verificati periodicamente per verificare se sono stati modificati. Con la convalida basata su catalogo, le immagini sorgente vengono controllate solo dopo la modifica del `catalog::TimeStamp` valore.

La convalida basata su catalogo è consigliata quando si utilizzano sia cataloghi di materiale che di vignettatura. La convalida basata sulla scadenza deve essere utilizzata quando alle richieste di rendering delle immagini viene fatto riferimento direttamente tramite percorso di vignettature.

## Proprietà {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 per selezionare la convalida basata sulla scadenza. 1 per selezionare la convalida della cache basata su catalogo.

## Predefinito {#section-e09f3af8b6b3497d963199988dc5345d}

Ereditato da `default::CacheValidationPolicy` se non definito o se vuoto.

## Consultate anche {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
