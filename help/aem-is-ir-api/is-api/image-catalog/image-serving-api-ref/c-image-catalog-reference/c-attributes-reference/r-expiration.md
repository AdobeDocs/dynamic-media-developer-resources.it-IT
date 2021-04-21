---
description: Tempo predefinito della cache del client per la durata. Fornisce un intervallo di scadenza predefinito nel caso in cui un particolare record di catalogo non contenga un valore di scadenza del catalogo valido.
solution: Experience Manager
title: Scadenza
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# Scadenza{#expiration}

Tempo predefinito della cache del client per la durata. Fornisce un intervallo di scadenza predefinito nel caso in cui un particolare record di catalogo non contenga un valore di catalogo valido::Expiration.

## Proprietà {#section-063be3b2f13a48a3a5ab8080718e9812}

Numero reale, 0 o superiore. Numero di ore fino alla scadenza dalla generazione dei dati di risposta. Imposta su 0 per far scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita in modo efficace il caching del client. Imposta su -1 per contrassegnare come `never expire`.

## Predefinito {#section-f55308b195c04083996f6717c8537634}

Ereditato da `default::Expiration` se non definito o se vuoto.

TTL (Time-to-Live) è la durata prima della scadenza della cache. Il TTL predefinito è di 10 ore.

## Consultate anche {#section-b2411d99ddb14115ad475d506efd8967}

[catalogo::Scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attributo::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attributo::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
