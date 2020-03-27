---
description: Attenzione a queste regole delle miniature.
seo-description: Attenzione a queste regole delle miniature.
seo-title: Regole per le miniature
solution: Experience Manager
title: Regole per le miniature
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Regole per le miniature{#thumbnail-rules}

Attenzione a queste regole delle miniature.

1. Se `catalog::ThumbType=Crop`necessario, l’immagine (ritagliata) viene ridimensionata fino a raggiungere le dimensioni più ridotte possibili pur continuando a coprire l’intero rect di destinazione. Se `catalog::ThumbType=Fit`necessario, l’immagine (ritagliata) viene ridimensionata fino alla dimensione massima possibile mentre l’intera immagine viene adattata al rettangolo di destinazione. Se `catalog::ThumbType=Texture`l’immagine (ritagliata) viene ridimensionata in base al rapporto tra `catalog::ThumbRes` e `catalog::Resolution`.
1. Allineare l’immagine ridimensionata al rect di destinazione in base a `attribute::ThumbHorizAlign` e `attribute::ThumbVertAlign`.
1. Ritagliate il risultato sul rettangolo di destinazione.

