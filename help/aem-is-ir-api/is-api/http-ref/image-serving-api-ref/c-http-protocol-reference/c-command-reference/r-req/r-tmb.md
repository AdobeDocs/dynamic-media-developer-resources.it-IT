---
description: Immagine miniatura. Richiede i dati immagine formattati e dimensionati utilizzando i criteri delle miniature del catalogo.
solution: Experience Manager
title: tam
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# tam{#tmb}

Immagine miniatura. Richiede i dati immagine formattati e dimensionati utilizzando i criteri delle miniature del catalogo.

`req=tmb`

Il formato dei dati di risposta e il tipo MIME di risposta sono determinati da `fmt=`. Supporta tutti i comandi eccetto `fit=`.

Consultare [Ridimensionamento miniature](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

La risposta HTTP può essere memorizzata nella cache con il TTL in base a `catalog::Expiration`.
