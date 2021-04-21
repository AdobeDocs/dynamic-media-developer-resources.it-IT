---
description: Dimensione predefinita della visualizzazione.
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# DefaultPix{#defaultpix}

Dimensione predefinita della visualizzazione.

Il server vincola le immagini di risposta a non superare questa larghezza e altezza, se la richiesta non specifica esplicitamente la dimensione della visualizzazione utilizzando `wid=`, `hei=` o `scl=`.

## Proprietà {#section-c3e658cf82c540d986b118f74f0fe1b2}

Due numeri interi, pari a 0 o superiori, separati da una virgola. Larghezza e altezza in pixel. È possibile impostare uno o entrambi i valori su 0 per mantenerli senza vincoli.

Non si applica alle richieste nidificate/incorporate.

## Predefinito {#section-b7338b2bf5114fff83b0714a57b20639}

Ereditato da `default::DefaultPix` se non definito o se vuoto.

## Consultate anche {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [catalogo::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
