---
description: Dati mappa immagine. Nessuno o più elementi HTML <AREA> completi, ordinati in ordine crescente.
solution: Experience Manager
title: Mappa
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
TQID: 'https://experienceleague.adobe.com/JY0barcvbF72sTyYW4iIhjFE-8tfqtbI78PDccLcXV0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 2%

---

# Mappa{#map}

Dati mappa immagine. Nessuno o più elementi HTML `<AREA>` completi, ordinati in avanti e indietro.

Il server interpreta e può modificare gli attributi SHAPE e COORDS (SHAPE=CIRCLE non è supportato in questa release). Tutti gli altri attributi di `<AREA>` vengono passati senza modifiche. I valori di coordinate specificati con l&#39;attributo COORDS devono essere offset in pixel dall&#39;angolo superiore sinistro dell&#39;immagine di origine non modificata. (`%` coordinate non sono supportate in questa versione e potrebbero non essere elaborate correttamente).

## Proprietà {#section-f52d89fd399b4356ac05277e6c12f956}

Valore stringa di testo. Se specificato, deve essere uno o più elementi HTML `<AREA>` completi.

Questo campo partecipa alla localizzazione delle stringhe di testo. Per ulteriori informazioni, consultare [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) nella *documentazione sul protocollo HTTP*.

## Predefinito {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Nessuno.

## Consultate anche {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localizzazione stringa di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
