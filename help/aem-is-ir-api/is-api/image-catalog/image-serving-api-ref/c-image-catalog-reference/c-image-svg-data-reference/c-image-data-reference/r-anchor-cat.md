---
description: Ancoraggio immagine. Punto di origine quando questa immagine viene utilizzata come livello in un modello o in un'immagine composita.
solution: Experience Manager
title: Ancoraggio
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
TQID: 'https://experienceleague.adobe.com/OKTbXTF3uzVcQeLQIGIJhCukQFzdW5gZMzatSdWP7yY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 4%

---

# Ancoraggio{#anchor}

Ancoraggio immagine. Punto di origine quando questa immagine viene utilizzata come livello in un modello o in un&#39;immagine composita.

Definisce anche il punto centrale di default per la rotazione.

## Proprietà {#section-95740f14160744e7bc763094b8be40d8}

Due numeri interi separati da una virgola. Offset pixel relativo all&#39;angolo superiore sinistro dell&#39;immagine a risoluzione massima.

Sostituito da `anchor=` (che a sua volta può essere sostituito da `origin=`).

## Predefinito {#section-ca3a4cc837d643519eff15951f2b47a1}

Il punto centrale dell&#39;immagine viene utilizzato se il campo non è presente o se è vuoto e se si tratta di un record immagine valido (ovvero se `catalog::Path` è valido).

## Consultate anche {#section-f605d29c3f5d48ad8e2a374f11886f19}

[ancoraggio=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origine=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
