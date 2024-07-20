---
description: Dati mappa immagine. Nessuno o più elementi HTML <AREA> completi, ordinati in ordine crescente.
solution: Experience Manager
title: Mappa
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# Mappa{#map}

Dati mappa immagine. Nessuno o più elementi HTML `<AREA>` completi, ordinati in ordine crescente.

Il server interpreta e può modificare gli attributi SHAPE e COORDS (SHAPE=CIRCLE non è supportato in questa release). Tutti gli altri attributi di `<AREA>` vengono passati senza modifiche. I valori di coordinate specificati con l&#39;attributo COORDS devono essere offset in pixel dall&#39;angolo superiore sinistro dell&#39;immagine di origine non modificata. (`%` coordinate non sono supportate in questa versione e potrebbero non essere elaborate correttamente).

## Proprietà {#section-f52d89fd399b4356ac05277e6c12f956}

Valore stringa di testo. Se specificato, deve essere uno o più elementi HTML completi `<AREA>`.

Questo campo partecipa alla localizzazione delle stringhe di testo. Per ulteriori informazioni, consultare [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) nella *documentazione sul protocollo HTTP*.

## Predefinito {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Nessuno.

## Consultate anche {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localizzazione stringa di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
