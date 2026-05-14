---
description: Tieni presente queste regole per le miniature.
solution: Experience Manager
title: Regole miniature
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
TQID: 'https://experienceleague.adobe.com/2HjWzEcMFnTFzwDWz-Ld7wZ6FsFcq3gwaUFcSWgxPko'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# Regole miniature{#thumbnail-rules}

Tieni presente queste regole per le miniature.

1. Se `catalog::ThumbType=Crop`, l&#39;immagine (ritagliata) viene ridimensionata al minimo mentre copre l&#39;intero rettangolo di destinazione. Se `catalog::ThumbType=Fit`, l&#39;immagine (ritagliata) viene ridimensionata alla dimensione più grande possibile mentre l&#39;intera immagine viene ancora adattata al retto di destinazione. Se `catalog::ThumbType=Texture`, l&#39;immagine (ritagliata) viene ridimensionata in base al rapporto tra `catalog::ThumbRes` e `catalog::Resolution`.
1. Allineare l&#39;immagine ridimensionata al retto di destinazione in base a `attribute::ThumbHorizAlign` e `attribute::ThumbVertAlign`.
1. Ritagliare il risultato nel rettangolo di destinazione.
