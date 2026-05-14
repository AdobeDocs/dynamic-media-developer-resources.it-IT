---
description: I dati immagine intermedi prodotti da richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.
solution: Experience Manager
title: Cache di dati ausiliari
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
TQID: 'https://experienceleague.adobe.com/oRZFSXKaBE9q7liBPRVCheL-NPTriPJkWZFqgMBcoaQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# Cache di dati ausiliari{#auxiliary-data-caches}

I dati immagine intermedi prodotti da richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.

Nella cache dei dati di risposta vengono memorizzate anche le immagini ottenute da server HTTP esterni. Tali immagini vengono convalidate automaticamente con l’utility di convalida prima che venga generata la voce della cache.

[!DNL Platform Server] compila i dati del catalogo immagini per un accesso efficiente. Questi dati sono archiviati in `CS::CatalogCacheFolder`.
