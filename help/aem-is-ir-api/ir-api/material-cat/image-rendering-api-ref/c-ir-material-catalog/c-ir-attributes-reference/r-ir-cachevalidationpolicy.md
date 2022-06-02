---
title: CacheValidationPolicy
description: Criterio di convalida della cache del server. Specifica quando vengono convalidate le voci della cache lato server.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Criterio di convalida della cache del server. Specifica quando vengono convalidate le voci della cache lato server.

Con la convalida basata sulla scadenza, i materiali di origine e le vignette vengono controllati periodicamente per verificare se sono cambiate. Con la convalida basata su catalogo, le immagini sorgente vengono controllate solo dopo la `catalog::TimeStamp` valore modificato.

La convalida basata su catalogo è consigliata quando si utilizzano sia cataloghi di materiale che di vignette. La convalida basata sulla scadenza deve essere utilizzata quando nelle richieste di rendering delle immagini viene fatto riferimento alle vignette direttamente tramite percorso.

## Proprietà {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 per selezionare una convalida basata sulla scadenza. 1 per selezionare la convalida della cache basata su catalogo.

## Predefinito {#section-e09f3af8b6b3497d963199988dc5345d}

Ereditato da `default::CacheValidationPolicy` se non definito o se vuoto.

## Consultate anche {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
