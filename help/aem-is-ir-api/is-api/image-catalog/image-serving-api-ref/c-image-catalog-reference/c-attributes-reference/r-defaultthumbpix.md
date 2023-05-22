---
description: Dimensioni miniature predefinite. Utilizzato al posto dell’attributo DefaultPix per le richieste di miniature (req=tmb).
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1413da0-a68d-4345-928f-b532991966a8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# DefaultThumbPix{#defaultthumbpix}

Dimensioni miniature predefinite. Utilizzato al posto dell&#39;attributo::DefaultPix per le richieste di miniature (req=tmb).

Se viene richiesta una miniatura, il server limita le dimensioni delle immagini di risposta ai valori di larghezza e altezza specificati `req=tmb`) non specifica la dimensione in modo esplicito non specifica la dimensione di visualizzazione esplicitamente utilizzando `wid=`, `hei=`, o `scl=`.

## Proprietà {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Due numeri interi, 0 o maggiori, separati da una virgola. Larghezza e altezza in pixel. Uno o entrambi i valori possono essere impostati su 0 per mantenerli liberi.

Non si applica alle richieste nidificate/incorporate.

## Predefinito {#section-2c4a4f14540449638822913513170ff1}

Ereditato da `default::DefaultThumbPix` se non è definita o se è vuota.

## Consultate anche {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
