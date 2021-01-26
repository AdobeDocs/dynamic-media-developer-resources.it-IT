---
description: Attenzione a queste regole delle miniature.
seo-description: Attenzione a queste regole delle miniature.
seo-title: Regole per le miniature
solution: Experience Manager
title: Regole per le miniature
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Regole per le miniature{#thumbnail-rules}

Attenzione a queste regole delle miniature.

1. Se `catalog::ThumbType=Crop`, l&#39;immagine (ritagliata) viene ridimensionata fino alla dimensione più piccola possibile pur continuando a coprire l&#39;intero rect di destinazione. Se `catalog::ThumbType=Fit`, l&#39;immagine (ritagliata) viene ridimensionata fino alla dimensione massima possibile mentre l&#39;intera immagine viene comunque adattata al rettangolo di destinazione. Se `catalog::ThumbType=Texture`, l&#39;immagine (ritagliata) viene ridimensionata al rapporto tra `catalog::ThumbRes` e `catalog::Resolution`.
1. Allineate l&#39;immagine ridimensionata con il rect di destinazione in base a `attribute::ThumbHorizAlign` e `attribute::ThumbVertAlign`.
1. Ritagliate il risultato sul rettangolo di destinazione.

