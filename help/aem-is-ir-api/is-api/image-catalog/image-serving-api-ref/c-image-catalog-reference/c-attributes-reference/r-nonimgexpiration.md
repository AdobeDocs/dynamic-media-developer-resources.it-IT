---
description: TTL cache client per le risposte non basate su immagini. Fornisce l'intervallo di scadenza per alcune risposte non basate su immagini.
seo-description: TTL cache client per le risposte non basate su immagini. Fornisce l'intervallo di scadenza per alcune risposte non basate su immagini.
seo-title: NonImgExpiration
solution: Experience Manager
title: NonImgExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 19b37bd4-f7cf-4b5f-be1a-b2d9fda5b4b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# NonImgExpiration{#nonimgexpiration}

TTL cache client per le risposte non basate su immagini. Fornisce l&#39;intervallo di scadenza per alcune risposte non basate su immagini.

Fornisce l&#39;intervallo di scadenza per alcune risposte non basate su immagini, comprese quelle inviate in risposta ai comandi seguenti:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Proprietà {#section-d37e3113f4b1468b86b5a14e80d94c83}

Numero reale, 0 o superiore. Numero di ore fino alla scadenza dalla generazione dei dati di risposta. Impostate su 0 per scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita il caching client per le risposte immagine predefinite. Impostate su -1 per contrassegnare come *non scaduto*.

## Predefinito {#section-96981360c0234b7f824d2ff7c25a7954}

Ereditato da `default::NonImgExpiration` se non definito o se vuoto.

TTL (Time-To-Live) è la durata prima della scadenza della cache. Il valore predefinito TTL è 6 minuti.

## Consultate anche {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalogo::Scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
