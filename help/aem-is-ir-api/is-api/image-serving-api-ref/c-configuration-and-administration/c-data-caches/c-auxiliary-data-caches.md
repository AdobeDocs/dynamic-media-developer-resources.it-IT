---
description: I dati immagine intermedi prodotti dalle richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.
solution: Experience Manager
title: Memorizzazione in cache dei dati ausiliari
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# Memorizzazione in cache dei dati ausiliari{#auxiliary-data-caches}

I dati immagine intermedi prodotti dalle richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.

Le immagini ottenute da server HTTP esterni vengono memorizzate anche nella cache dei dati di risposta. Tali immagini vengono convalidate automaticamente con l&#39;utility validate prima che venga generata la voce cache.

Platform Server compila i dati del catalogo immagini per un accesso efficiente. Questi dati vengono memorizzati in `CS::CatalogCacheFolder`.
