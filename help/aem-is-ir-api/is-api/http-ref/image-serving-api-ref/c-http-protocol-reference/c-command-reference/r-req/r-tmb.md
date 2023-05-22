---
description: Immagine miniatura. Richiede dati immagine formattati e ridimensionati utilizzando i criteri delle miniature del catalogo.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---

# tmb{#tmb}

Immagine miniatura. Richiede dati immagine formattati e ridimensionati utilizzando i criteri delle miniature del catalogo.

`req=tmb`

Il formato dei dati di risposta e il tipo di MIME di risposta sono determinati da `fmt=`. Supporta tutti i comandi tranne `fit=`.

Consulta [Ridimensionamento miniature](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.
