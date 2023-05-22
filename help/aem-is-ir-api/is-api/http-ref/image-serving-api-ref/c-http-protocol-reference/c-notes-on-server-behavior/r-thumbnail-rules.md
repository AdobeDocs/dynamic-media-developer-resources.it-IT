---
description: Tieni presente queste regole per le miniature.
solution: Experience Manager
title: Regole miniature
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# Regole miniature{#thumbnail-rules}

Tieni presente queste regole per le miniature.

1. Se `catalog::ThumbType=Crop`, quindi l’immagine (ritagliata) viene ridimensionata alla dimensione più piccola possibile coprendo comunque l’intero rettangolo di destinazione. Se `catalog::ThumbType=Fit`, quindi l&#39;immagine (ritagliata) viene ridimensionata alla dimensione più grande possibile mentre l&#39;intera immagine viene ancora adattata al retto di destinazione. Se `catalog::ThumbType=Texture`, l’immagine (ritagliata) viene ridimensionata in base al rapporto tra `catalog::ThumbRes` a `catalog::Resolution`.
1. Allinea l&#39;immagine ridimensionata al retto di destinazione in base a `attribute::ThumbHorizAlign` e `attribute::ThumbVertAlign`.
1. Ritagliare il risultato nel rettangolo di destinazione.
