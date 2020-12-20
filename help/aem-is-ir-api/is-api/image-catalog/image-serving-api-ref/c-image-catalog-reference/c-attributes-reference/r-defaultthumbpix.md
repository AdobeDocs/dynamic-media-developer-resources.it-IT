---
description: Dimensione predefinita miniatura. Utilizzato al posto dell'attributo DefaultPix per le richieste di miniature (req=tmb).
seo-description: Dimensione predefinita miniatura. Utilizzato al posto dell'attributo DefaultPix per le richieste di miniature (req=tmb).
seo-title: DefaultThumbPix
solution: Experience Manager
title: DefaultThumbPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b310aab-6d38-45f3-a3e7-b074a8e7a795
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# DefaultThumbPix{#defaultthumbpix}

Dimensione predefinita miniatura. Utilizzato al posto di attribute::DefaultPix per le richieste di miniature (req=tmb).

Il server vincola le immagini di risposta ad avere una larghezza e altezza massime, se una richiesta di miniatura ( `req=tmb`) non specifica esplicitamente la dimensione della visualizzazione utilizzando `wid=`, `hei=` o `scl=`.

## Proprietà {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Due numeri interi, pari a 0 o superiori, separati da virgola. Larghezza e altezza in pixel. Uno o entrambi i valori possono essere impostati su 0 per mantenerli non vincolati.

Non si applica alle richieste nidificate/incorporate.

## Predefinito {#section-2c4a4f14540449638822913513170ff1}

Ereditato da `default::DefaultThumbPix` se non definito o se vuoto.

## Consultate anche {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
