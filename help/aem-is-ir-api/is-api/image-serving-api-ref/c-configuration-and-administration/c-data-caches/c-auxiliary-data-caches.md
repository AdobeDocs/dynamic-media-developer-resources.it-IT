---
description: I dati immagine intermedi prodotti dalle richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.
solution: Experience Manager
title: Memorizzazione in cache dei dati ausiliari
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Memorizzazione in cache dei dati ausiliari{#auxiliary-data-caches}

I dati immagine intermedi prodotti dalle richieste di Image Server e Image Rendering nidificate/incorporate possono essere memorizzati nella cache specificando cache=on nella richiesta nidificata/incorporata. Questi dati vengono memorizzati in formato proprietario nella cache dei dati di risposta.

Le immagini ottenute da server HTTP esterni vengono memorizzate anche nella cache dei dati di risposta. Tali immagini vengono convalidate automaticamente con l&#39;utility validate prima che venga generata la voce cache.

Platform Server compila i dati del catalogo immagini per un accesso efficiente. Questi dati vengono memorizzati in `CS::CatalogCacheFolder`.
