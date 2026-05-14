---
title: CacheValidationPolicy
description: Criteri di convalida della cache del server. Specifica quando vengono convalidate le voci della cache lato server.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
TQID: 'https://experienceleague.adobe.com/8WipxBM2HngJP5f8LOJmFPA5jZTyJt6Q5P9mZnzDPsY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Criteri di convalida della cache del server. Specifica quando vengono convalidate le voci della cache lato server.

Con la convalida basata sulla scadenza, i materiali di base e le vignette vengono controllati periodicamente per verificare se sono cambiati. Con la convalida basata sul catalogo, le immagini di origine vengono controllate solo dopo la modifica del valore `catalog::TimeStamp`.

La convalida basata sul catalogo è consigliata quando si utilizzano cataloghi di materiale e vignettatura. La convalida basata sulla scadenza deve essere utilizzata quando nelle richieste di Image Rendering si fa riferimento direttamente alle vignettature per percorso.

## Proprietà {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 per selezionare la convalida basata sulla scadenza. 1 per selezionare la convalida della cache basata su catalogo.

## Predefinito {#section-e09f3af8b6b3497d963199988dc5345d}

Ereditato da `default::CacheValidationPolicy` se non definito o se vuoto.

## Consultate anche {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalogo::Timestamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
