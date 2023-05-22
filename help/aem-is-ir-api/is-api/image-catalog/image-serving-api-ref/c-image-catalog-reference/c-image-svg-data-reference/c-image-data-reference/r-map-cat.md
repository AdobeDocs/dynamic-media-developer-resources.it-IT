---
description: Dati mappa immagine. Nessuno o più HTML completi <area> elementi, ordinati dall'inizio alla fine.
solution: Experience Manager
title: Mappa
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# Mappa{#map}

Dati mappa immagine. Nessuno o più HTML completi `<AREA>` elementi, ordinati dall&#39;inizio alla fine.

Il server interpreterà e potrebbe modificare gli attributi SHAPE e COORDS. (SHAPE=CIRCLE non supportato in questa versione). Tutti gli altri attributi di `<AREA>` vengono trasmesse senza modifiche. I valori di coordinate specificati con l&#39;attributo COORDS devono essere offset in pixel dall&#39;angolo superiore sinistro dell&#39;immagine di origine non modificata. (`%` Le coordinate non sono supportate in questa versione e potrebbero non essere elaborate correttamente.)

## Proprietà {#section-f52d89fd399b4356ac05277e6c12f956}

Valore stringa di testo. Se specificato, deve essere uno o più HTML completi `<AREA>` elementi.

Questo campo partecipa alla localizzazione delle stringhe di testo. Fai riferimento a [Localizzazione stringa di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) nel *Riferimento protocollo HTTP* per i dettagli.

## Predefinito {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Nessuno.

## Consultate anche {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map= mappa](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localizzazione stringa di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
