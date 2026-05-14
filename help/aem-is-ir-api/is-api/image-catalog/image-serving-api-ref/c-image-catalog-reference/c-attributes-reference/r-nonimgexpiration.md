---
description: TTL della cache client per risposte non di immagine. Specifica l'intervallo di scadenza per alcune risposte non di tipo immagine.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
TQID: 'https://experienceleague.adobe.com/A21KkwsYFIMp9Pw0WyX-c-3UVlFg2FacObh2jjRVTwA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
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
