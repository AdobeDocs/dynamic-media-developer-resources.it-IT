---
description: Dimensioni predefinite della visualizzazione.
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 709fb2a1-1b9d-421e-9a65-5f5c74390ce3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# DefaultPix{#defaultpix}

Dimensioni predefinite della visualizzazione.

Il server vincola le dimensioni delle immagini di risposta ai valori di larghezza e altezza specificati, se nella richiesta non sono specificate esplicitamente le dimensioni di visualizzazione tramite `wid=`, `hei=`, o `scl=`.

## Proprietà {#section-c3e658cf82c540d986b118f74f0fe1b2}

Due numeri interi, 0 o maggiori, separati da una virgola. Larghezza e altezza in pixel. Uno o entrambi i valori possono essere impostati su 0 per mantenerli liberi.

Non si applica alle richieste nidificate/incorporate.

## Predefinito {#section-b7338b2bf5114fff83b0714a57b20639}

Ereditato da `default::DefaultPix` se non è definita o se è vuota.

## Consultate anche {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [catalogo::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
