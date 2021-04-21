---
description: Dimensione predefinita miniatura. Utilizzato al posto dell'attributo DefaultPix per le richieste di miniature (req=tmb).
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# DefaultThumbPix{#defaultthumbpix}

Dimensione predefinita miniatura. Utilizzato al posto dell&#39;attributo::DefaultPix per le richieste di miniature (req=tmb).

Il server vincola le immagini di risposta a non superare questa larghezza e altezza, se una richiesta di miniatura ( `req=tmb`) non specifica esplicitamente la dimensione della visualizzazione utilizzando esplicitamente `wid=`, `hei=` o `scl=`.

## Proprietà {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Due numeri interi, pari a 0 o superiori, separati da una virgola. Larghezza e altezza in pixel. È possibile impostare uno o entrambi i valori su 0 per mantenerli senza vincoli.

Non si applica alle richieste nidificate/incorporate.

## Predefinito {#section-2c4a4f14540449638822913513170ff1}

Ereditato da `default::DefaultThumbPix` se non definito o se vuoto.

## Consultate anche {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [attributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
