---
description: Immagine miniatura. Richiede i dati immagine formattati e dimensionati utilizzando i criteri delle miniature del catalogo.
seo-description: Immagine miniatura. Richiede i dati immagine formattati e dimensionati utilizzando i criteri delle miniature del catalogo.
seo-title: tam
solution: Experience Manager
title: tam
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# tmb{#tmb}

Immagine miniatura. Richiede i dati immagine formattati e dimensionati utilizzando i criteri delle miniature del catalogo.

`req=tmb`

Il formato dei dati di risposta e il tipo MIME di risposta sono determinati da `fmt=`. Supporta tutti i comandi eccetto `fit=`.

Consultare [Ridimensionamento miniature](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

La risposta HTTP può essere memorizzata nella cache con il TTL in base a `catalog::Expiration`.
