---
description: Dati mappa immagine. Nessuno o più elementi HTML completi <AREA>, ordinati in modalità front-to-back.
solution: Experience Manager
title: Mappa
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 5%

---

# Mappa{#map}

Dati mappa immagine. Nessuno o più elementi HTML completi `<AREA>`, ordinati fronte-retro.

Il server interpreterà e può modificare gli attributi SHAPE e COORDS. (SHAPE=CIRCLE non è supportato in questa versione.) Tutti gli altri attributi di `<AREA>` vengono passati senza modifiche. I valori di coordinate specificati con l&#39;attributo COORDS devono essere offset pixel dall&#39;angolo in alto a sinistra dell&#39;immagine sorgente non modificata. (`%` le coordinate non sono supportate in questa versione e potrebbero non essere elaborate correttamente).

## Proprietà {#section-f52d89fd399b4356ac05277e6c12f956}

Valore stringa di testo. Se specificato, deve essere uno o più elementi HTML completi `<AREA>`.

Questo campo partecipa alla localizzazione delle stringhe di testo. Per ulteriori informazioni, consulta [Localizzazione delle stringhe di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in *Riferimento al protocollo HTTP* .

## Predefinito {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Nessuno.

## Consultate anche {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ,  [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), localizzazione di stringhe di  [testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
