---
description: Rispondi al limite delle dimensioni dell’immagine. Larghezza e altezza massime dell'immagine di risposta che possono essere restituite al client.
seo-description: Rispondi al limite delle dimensioni dell’immagine. Larghezza e altezza massime dell'immagine di risposta che possono essere restituite al client.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8fc5e032-cfbb-40b5-9c3a-a2ec1bc4c3e2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# MaxPix{#maxpix}

Rispondi al limite delle dimensioni dell’immagine. Larghezza e altezza massime dell&#39;immagine di risposta che possono essere restituite al client.

Il server restituisce un errore se una richiesta causerebbe un&#39;immagine di risposta la cui larghezza e/o altezza è maggiore di `attribute::MaxSize`.

## Proprietà {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Due numeri interi, maggiori di 0, separati da virgola. Larghezza e altezza in pixel. Può anche essere impostato su 0,0 per consentire qualsiasi dimensione immagine di risposta senza limitazioni.

## Predefinito {#section-45b38dc661854d11b97df5709f4f3434}

Ereditato da default::MaxPix se non definito o se vuoto.

## Consultate anche {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
