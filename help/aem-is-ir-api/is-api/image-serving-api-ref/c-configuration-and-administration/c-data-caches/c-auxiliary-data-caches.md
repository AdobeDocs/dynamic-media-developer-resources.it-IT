---
description: I dati immagine intermedi prodotti da richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.
solution: Experience Manager
title: Cache di dati ausiliari
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Cache di dati ausiliari{#auxiliary-data-caches}

I dati immagine intermedi prodotti da richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.

Nella cache dei dati di risposta vengono memorizzate anche le immagini ottenute da server HTTP esterni. Tali immagini vengono convalidate automaticamente con l’utility di convalida prima che venga generata la voce della cache.

[!DNL Platform Server] compila i dati del catalogo immagini per un accesso efficiente. Questi dati sono archiviati in `CS::CatalogCacheFolder`.
