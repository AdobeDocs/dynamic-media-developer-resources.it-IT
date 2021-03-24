---
description: Criterio di convalida della cache del server. Specifica quando vengono convalidate le voci della cache lato server.
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

Criterio di convalida della cache del server. Specifica quando vengono convalidate le voci della cache lato server.

Con la convalida basata sulla scadenza, i materiali di origine e le vignette vengono controllati periodicamente per verificare se sono cambiate. Con la convalida basata su catalogo, le immagini sorgente vengono controllate solo dopo la modifica del valore `catalog::TimeStamp`.

La convalida basata su catalogo è consigliata quando si utilizzano sia cataloghi di materiale che di vignette. La convalida basata sulla scadenza deve essere utilizzata quando nelle richieste di rendering delle immagini viene fatto riferimento alle vignette direttamente tramite percorso.

## Proprietà {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 per selezionare una convalida basata sulla scadenza. 1 per selezionare la convalida della cache basata su catalogo.

## Predefinito {#section-e09f3af8b6b3497d963199988dc5345d}

Ereditato da `default::CacheValidationPolicy` se non definito o se vuoto.

## Consultate anche {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
