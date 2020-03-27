---
description: Rispondi al limite delle dimensioni dell’immagine. Larghezza e altezza massime dell'immagine di risposta che possono essere restituite al client.
seo-description: Rispondi al limite delle dimensioni dell’immagine. Larghezza e altezza massime dell'immagine di risposta che possono essere restituite al client.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MaxPix{#maxpix}

Rispondi al limite delle dimensioni dell’immagine. Larghezza e altezza massime dell&#39;immagine di risposta che possono essere restituite al client.

Il server restituisce un errore se una richiesta causerebbe un&#39;immagine di risposta la cui larghezza o altezza è maggiore di `attribute::MaxPix`.

## Proprietà {#section-b175425b9e9f48e0b1a71640f6a9e936}

Due numeri interi, maggiori di 0, separati da virgola. Larghezza e altezza in pixel. Può essere impostato anche `0,0` per consentire qualsiasi dimensione immagine di risposta senza limitazioni.

## Predefinito {#section-1003537434da432fb2af100ecdbf9d72}

Ereditato da `default::MaxPix` se non definito o se vuoto.

## Consultate anche {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
