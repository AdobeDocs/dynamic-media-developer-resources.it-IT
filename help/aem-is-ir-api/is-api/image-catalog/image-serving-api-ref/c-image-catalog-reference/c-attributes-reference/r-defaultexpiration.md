---
description: TTL cache client per le risposte immagine predefinite. Fornisce l’intervallo di scadenza per le risposte immagine predefinite (risposte che restituiscono un’immagine predefinita specificata con defaultImage= o attribute DefaultImage).
seo-description: TTL cache client per le risposte immagine predefinite. Fornisce l’intervallo di scadenza per le risposte immagine predefinite (risposte che restituiscono un’immagine predefinita specificata con defaultImage= o attribute DefaultImage).
seo-title: DefaultExpiration
solution: Experience Manager
title: DefaultExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# DefaultExpiration{#defaultexpiration}

TTL cache client per le risposte immagine predefinite. Fornisce l’intervallo di scadenza per le risposte immagine predefinite (risposte che restituiscono un’immagine predefinita specificata con defaultImage= o attribute::DefaultImage).

Applicata solo quando l&#39;immagine predefinita non è associata a un record catalogo o quando il record catalogo immagini predefinito non fornisce un valore specifico `catalog::Expiration`.

## Proprietà {#section-e564512476604fd7b964f9f2903d6d33}

Numero reale, 0 o superiore. Numero di ore fino alla scadenza dalla generazione dei dati di risposta. Impostate su 0 per scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita il caching client per le risposte immagine predefinite. Impostare su `-1` per contrassegnare come `never expire`.

## Predefinito {#section-131cd32c2e214391857dba5af321f8cd}

Ereditato da `default::DefaultExpiration` se non definito o se vuoto.

TTL (Time-To-Live) è la durata prima della scadenza della cache. Il valore predefinito TTL è 1 ora.

## Consultate anche {#section-d8642c22e3d947129367dd76366963d6}

[catalogo::Scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
