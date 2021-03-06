---
description: Dimensione predefinita dell'immagine di rendering. Il server vincola le immagini di risposta a non superare questa larghezza e altezza, se la richiesta non specifica esplicitamente la dimensione di visualizzazione utilizzando wid= o hei=.
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# DefaultPix{#defaultpix}

Dimensione predefinita dell&#39;immagine di rendering. Il server vincola le immagini di risposta a non superare questa larghezza e altezza, se la richiesta non specifica esplicitamente la dimensione di visualizzazione utilizzando wid= o hei=.

## Proprietà {#section-9dc5474fc75842308796ab6440b29611}

Due numeri interi, pari a 0 o superiori, separati da una virgola. Larghezza e altezza in pixel. È possibile impostare uno o entrambi i valori su 0 per mantenerli senza vincoli.

Non applicabile alle richieste nidificate/incorporate.

## Predefinito {#section-1935781c561e4679aa87a5bcced8df90}

Ereditato da `default::DefaultPix` se non definito o se vuoto.

## Consultate anche {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [attributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
