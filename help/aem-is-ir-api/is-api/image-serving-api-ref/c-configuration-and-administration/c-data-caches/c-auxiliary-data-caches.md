---
description: I dati immagine intermedi prodotti dalle richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.
seo-description: I dati immagine intermedi prodotti dalle richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.
seo-title: Memorizzazione in cache dei dati ausiliari
solution: Experience Manager
title: Memorizzazione in cache dei dati ausiliari
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Memorizzazione in cache dei dati ausiliari{#auxiliary-data-caches}

I dati immagine intermedi prodotti dalle richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.

Le immagini ottenute da server HTTP esterni vengono memorizzate anche nella cache dei dati di risposta. Tali immagini vengono convalidate automaticamente con l&#39;utility validate prima che venga generata la voce cache.

Platform Server compila i dati del catalogo immagini per un accesso efficiente. Questi dati vengono memorizzati in `CS::CatalogCacheFolder`.
