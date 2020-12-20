---
description: I dati immagine intermedi generati dalle richieste nidificate/incorporate di Image Server e di Image Rendering possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.
seo-description: I dati immagine intermedi generati dalle richieste nidificate/incorporate di Image Server e di Image Rendering possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.
seo-title: Cache dati ausiliari
solution: Experience Manager
title: Cache dati ausiliari
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# Cache dati ausiliari{#auxiliary-data-caches}

I dati immagine intermedi generati dalle richieste nidificate/incorporate di Image Server e di Image Rendering possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.

Le immagini ottenute da server HTTP esterni vengono memorizzate anche nella cache dei dati di risposta. Tali immagini vengono convalidate automaticamente con l&#39;utility validate prima della generazione della voce della cache.

Platform Server compila i dati del catalogo immagini per un accesso efficiente. Questi dati vengono memorizzati in `CS::CatalogCacheFolder`.
