---
title: MaxPix
description: Limite di dimensione dell'immagine della risposta. Larghezza e altezza massime dell'immagine di risposta che possono essere restituite al client.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# MaxPix{#maxpix}

Limite di dimensione dell&#39;immagine della risposta. Larghezza e altezza massime dell&#39;immagine di risposta che possono essere restituite al client.

Il server restituisce un errore se una richiesta causa un&#39;immagine di risposta con larghezza e/o altezza maggiori di `attribute::MaxSize`.

## Proprietà {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Due numeri interi, maggiori di 0, separati da una virgola. Larghezza e altezza in pixel. Può anche essere impostato su 0,0 per consentire qualsiasi dimensione dell&#39;immagine di risposta senza limitazioni.

## Predefinito {#section-45b38dc661854d11b97df5709f4f3434}

Ereditato da default::MaxPix se non definito o se vuoto.

## Consultate anche {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
