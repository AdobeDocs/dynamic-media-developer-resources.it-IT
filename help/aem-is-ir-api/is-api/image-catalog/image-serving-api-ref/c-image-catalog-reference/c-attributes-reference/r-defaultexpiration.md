---
description: TTL della cache client per le risposte immagine predefinite. Specifica l'intervallo di scadenza per le risposte immagine predefinite (risposte che restituiscono un'immagine predefinita specificata con defaultImage= o con l'attributo DefaultImage).
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 1%

---

# DefaultExpiration{#defaultexpiration}

TTL della cache client per le risposte immagine predefinite. Specifica l&#39;intervallo di scadenza per le risposte immagine predefinite (risposte che restituiscono un&#39;immagine predefinita specificata con defaultImage= o attribute::DefaultImage).

Applicato solo quando l’immagine predefinita non è associata a un record catalogo o quando il record catalogo immagini predefinito non fornisce un `catalog::Expiration` valore.

## Proprietà {#section-e564512476604fd7b964f9f2903d6d33}

Numero reale, 0 o superiore. Numero di ore mancanti alla scadenza dalla generazione dei dati di risposta. Impostate questo valore su 0 per far scadere immediatamente l&#39;immagine di risposta e disabilitare quindi la memorizzazione nella cache del client per le risposte immagine predefinite. Imposta su `-1` da contrassegnare come `never expire`.

## Predefinito {#section-131cd32c2e214391857dba5af321f8cd}

Ereditato da `default::DefaultExpiration` se non è definita o se è vuota.

TTL (Time-To-Live) è la durata prima della scadenza della cache. Il valore TTL predefinito è 1 ora.

## Consultate anche {#section-d8642c22e3d947129367dd76366963d6}

[catalogo::scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
