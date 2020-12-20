---
description: Miniatura. Richiede dati immagine formattati e dimensionati utilizzando i criteri delle miniature del catalogo.
seo-description: Miniatura. Richiede dati immagine formattati e dimensionati utilizzando i criteri delle miniature del catalogo.
seo-title: tmb
solution: Experience Manager
title: tmb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---


# tmb{#tmb}

Miniatura. Richiede dati immagine formattati e dimensionati utilizzando i criteri delle miniature del catalogo.

`req=tmb`

Il formato dei dati di risposta e il tipo MIME di risposta sono determinati da `fmt=`. Supporta tutti i comandi eccetto `fit=`.

Vedere [Ridimensionamento delle miniature](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

La risposta HTTP può essere memorizzata nella cache con TTL in base a `catalog::Expiration`.
