---
description: I dati immagine intermedi prodotti dalle richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.
solution: Experience Manager
title: Memorizzazione in cache dei dati ausiliari
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Memorizzazione in cache dei dati ausiliari{#auxiliary-data-caches}

I dati immagine intermedi prodotti dalle richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.

Le immagini ottenute da server HTTP esterni vengono memorizzate anche nella cache dei dati di risposta. Tali immagini vengono convalidate automaticamente con l&#39;utility validate prima che venga generata la voce cache.

Platform Server compila i dati del catalogo immagini per un accesso efficiente. Questi dati vengono memorizzati in `CS::CatalogCacheFolder`.
