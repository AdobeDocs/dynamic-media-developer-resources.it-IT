---
description: Tieni presente queste regole per le miniature.
solution: Experience Manager
title: Regole per le miniature
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Regole per le miniature{#thumbnail-rules}

Tieni presente queste regole per le miniature.

1. Se `catalog::ThumbType=Crop`, l&#39;immagine (ritagliata) viene ridimensionata in base alle dimensioni più piccole possibili, coprendo comunque l&#39;intera correzione target. Se `catalog::ThumbType=Fit`, l&#39;immagine (ritagliata) viene ridimensionata in base alle dimensioni massime possibili, mantenendo l&#39;intera immagine nella direzione di destinazione. Se `catalog::ThumbType=Texture`, l&#39;immagine (ritagliata) viene ridimensionata in base al rapporto tra `catalog::ThumbRes` e `catalog::Resolution`.
1. Allinea l’immagine in scala con il corretto di destinazione in base a `attribute::ThumbHorizAlign` e `attribute::ThumbVertAlign`.
1. Ritagliare il risultato sul corretto di destinazione.
