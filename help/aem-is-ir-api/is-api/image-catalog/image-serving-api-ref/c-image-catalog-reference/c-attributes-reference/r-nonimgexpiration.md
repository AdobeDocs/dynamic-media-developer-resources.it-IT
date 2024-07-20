---
description: TTL della cache client per risposte non di immagine. Specifica l'intervallo di scadenza per alcune risposte non di tipo immagine.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# NonImgExpiration{#nonimgexpiration}

TTL della cache client per risposte non di immagine. Specifica l&#39;intervallo di scadenza per alcune risposte non di tipo immagine.

Specifica l&#39;intervallo di scadenza per alcune risposte non di tipo immagine, incluse quelle inviate in risposta ai seguenti comandi:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Proprietà {#section-d37e3113f4b1468b86b5a14e80d94c83}

Numero reale, 0 o superiore. Numero di ore mancanti alla scadenza dalla generazione dei dati di risposta. Impostate questo valore su 0 per far scadere immediatamente l&#39;immagine di risposta e disabilitare quindi la memorizzazione nella cache del client per le risposte immagine predefinite. Imposta su -1 per contrassegnare come *senza scadenza*.

## Predefinito {#section-96981360c0234b7f824d2ff7c25a7954}

Ereditato da `default::NonImgExpiration` se non definito o se vuoto.

TTL (Time-To-Live) è la durata prima della scadenza della cache. Il valore TTL predefinito è 6 minuti.

## Consultate anche {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalogo::Scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
