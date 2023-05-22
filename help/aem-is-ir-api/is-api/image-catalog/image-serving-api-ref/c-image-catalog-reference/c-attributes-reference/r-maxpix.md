---
description: Limite dimensioni immagine di risposta. Larghezza e altezza massime per l’immagine da restituire al client.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# MaxPix{#maxpix}

Limite dimensioni immagine di risposta. Larghezza e altezza massime per l’immagine da restituire al client.

Il server restituisce un errore se una richiesta causerebbe un’immagine di risposta con larghezza o altezza maggiore di `attribute::MaxPix`.

## Proprietà {#section-b175425b9e9f48e0b1a71640f6a9e936}

Due numeri interi, maggiori di 0, separati da una virgola. Larghezza e altezza in pixel. Può essere impostato anche su `0,0` per consentire qualsiasi dimensione di immagine di risposta senza limitazioni.

## Predefinito {#section-1003537434da432fb2af100ecdbf9d72}

Ereditato da `default::MaxPix` se non è definita o se è vuota.

## Consultate anche {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
