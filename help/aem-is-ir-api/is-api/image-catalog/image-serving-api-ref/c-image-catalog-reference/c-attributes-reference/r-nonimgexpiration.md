---
description: TTL della cache client per le risposte non basate su immagini. Fornisce l'intervallo di scadenza per alcune risposte non basate su immagini.
seo-description: TTL della cache client per le risposte non basate su immagini. Fornisce l'intervallo di scadenza per alcune risposte non basate su immagini.
seo-title: NonImgExpiration
solution: Experience Manager
title: NonImgExpiration
uuid: 19b37bd4-f7cf-4b5f-be1a-b2d9fda5b4b1
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# NonImgExpiration{#nonimgexpiration}

TTL della cache client per le risposte non basate su immagini. Fornisce l&#39;intervallo di scadenza per alcune risposte non basate su immagini.

Fornisce l&#39;intervallo di scadenza per alcune risposte non basate su immagini, incluse quelle inviate in risposta ai seguenti comandi:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Proprietà {#section-d37e3113f4b1468b86b5a14e80d94c83}

Numero reale, 0 o superiore. Numero di ore fino alla scadenza dalla generazione dei dati di risposta. Imposta su 0 per far scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita in modo efficace la memorizzazione in cache del client per le risposte alle immagini predefinite. Imposta su -1 per contrassegnare come *non scade*.

## Predefinito {#section-96981360c0234b7f824d2ff7c25a7954}

Ereditato da `default::NonImgExpiration` se non definito o se vuoto.

TTL (Time-to-Live) è la durata prima della scadenza della cache. Il TTL predefinito è 6 minuti.

## Consultate anche {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalogo::Scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
