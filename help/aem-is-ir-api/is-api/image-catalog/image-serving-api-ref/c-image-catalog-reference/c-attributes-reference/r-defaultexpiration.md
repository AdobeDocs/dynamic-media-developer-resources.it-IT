---
description: TTL della cache client per le risposte immagine predefinite. Fornisce l'intervallo di scadenza per le risposte immagine predefinite (risposte che restituiscono un'immagine predefinita specificata con defaultImage= o attributo DefaultImage).
solution: Experience Manager
title: ScadenzaPredefinita
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# DefaultExpiration{#defaultexpiration}

TTL della cache client per le risposte immagine predefinite. Fornisce l&#39;intervallo di scadenza per le risposte immagine predefinite (risposte che restituiscono un&#39;immagine predefinita specificata con defaultImage= o attribute::DefaultImage).

Applicato solo quando l&#39;immagine predefinita non è associata a un record di catalogo o quando il record di catalogo immagini predefinito non fornisce un valore specifico `catalog::Expiration`.

## Proprietà {#section-e564512476604fd7b964f9f2903d6d33}

Numero reale, 0 o superiore. Numero di ore fino alla scadenza dalla generazione dei dati di risposta. Imposta su 0 per far scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita in modo efficace la memorizzazione in cache del client per le risposte alle immagini predefinite. Impostare su `-1` per contrassegnare come `never expire`.

## Predefinito {#section-131cd32c2e214391857dba5af321f8cd}

Ereditato da `default::DefaultExpiration` se non definito o se vuoto.

TTL (Time-to-Live) è la durata prima della scadenza della cache. Il TTL predefinito è 1 ora.

## Consultate anche {#section-d8642c22e3d947129367dd76366963d6}

[catalogo::Scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
