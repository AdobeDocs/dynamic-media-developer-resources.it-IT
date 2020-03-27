---
description: Durata predefinita cache client. Fornisce un intervallo di scadenza predefinito nel caso in cui un determinato record di catalogo non contenga un valore di scadenza valido per il catalogo.
seo-description: Durata predefinita cache client. Fornisce un intervallo di scadenza predefinito nel caso in cui un determinato record di catalogo non contenga un valore di scadenza valido per il catalogo.
seo-title: Scadenza
solution: Experience Manager
title: Scadenza
topic: Scene7 Image Serving - Image Rendering API
uuid: 26b2abee-8bd1-4011-90ff-f5143826ac0d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Scadenza{#expiration}

Durata predefinita cache client. Fornisce un intervallo di scadenza predefinito nel caso in cui un determinato record di catalogo non contenga un valore di catalogo valido::Expiration.

## Proprietà {#section-063be3b2f13a48a3a5ab8080718e9812}

Numero reale, 0 o superiore. Numero di ore fino alla scadenza dalla generazione dei dati di risposta. Impostate su 0 per scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita in modo efficace il caching del client. Impostare su -1 per contrassegnare come `never expire`.

## Predefinito {#section-f55308b195c04083996f6717c8537634}

Ereditato da `default::Expiration` se non definito o se vuoto.

TTL (Time-To-Live) è la durata prima della scadenza della cache. Il valore predefinito TTL è 10 ore.

## Consultate anche {#section-b2411d99ddb14115ad475d506efd8967}

[catalogo::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
