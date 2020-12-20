---
description: Dati mappa immagine. Nessuno o più elementi HTML <AREA> completi, ordinati fronte/retro.
seo-description: Dati mappa immagine. Nessuno o più elementi HTML <AREA> completi, ordinati fronte/retro.
seo-title: Mappa
solution: Experience Manager
title: Mappa
topic: Scene7 Image Serving - Image Rendering API
uuid: 674a7a74-91bf-41c4-ab74-a5cb4f8abe1d
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 5%

---


# Mappa{#map}

Dati mappa immagine. Nessuno o più elementi HTML `<AREA>` completi, ordinati fronte/retro.

Il server interpreterà e potrebbe modificare gli attributi SHAPE e COORDS. SHAPE=CIRCLE non è supportato in questa versione. Tutti gli altri attributi di `<AREA>` vengono passati senza modifiche. I valori di coordinate specificati con l’attributo COORDS devono essere offset di pixel dall’angolo superiore sinistro dell’immagine sorgente non modificata. (`%` le coordinate non sono supportate in questa versione e potrebbero non essere elaborate correttamente).

## Proprietà {#section-f52d89fd399b4356ac05277e6c12f956}

Valore stringa di testo. Se specificato, deve essere uno o più elementi HTML `<AREA>` completi.

Questo campo partecipa alla localizzazione delle stringhe di testo. Per ulteriori informazioni, consultare [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in *HTTP Protocol Reference*.

## Predefinito {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Nessuno.

## Consultate anche {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ,  [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), Localizzazione stringa di  [testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
