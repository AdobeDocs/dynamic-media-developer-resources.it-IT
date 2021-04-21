---
description: Limite di dimensione dell'immagine della risposta. Larghezza e altezza massime dell'immagine di risposta che possono essere restituite al client.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# MaxPix{#maxpix}

Limite di dimensione dell&#39;immagine della risposta. Larghezza e altezza massime dell&#39;immagine di risposta che possono essere restituite al client.

Il server restituisce un errore se una richiesta causa un&#39;immagine di risposta la cui larghezza o altezza è maggiore di `attribute::MaxPix`.

## Proprietà {#section-b175425b9e9f48e0b1a71640f6a9e936}

Due numeri interi, maggiori di 0, separati da una virgola. Larghezza e altezza in pixel. Può essere impostato anche su `0,0` per consentire qualsiasi dimensione dell&#39;immagine di risposta senza limitazioni.

## Predefinito {#section-1003537434da432fb2af100ecdbf9d72}

Ereditato da `default::MaxPix` se non definito o se vuoto.

## Consultate anche {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
