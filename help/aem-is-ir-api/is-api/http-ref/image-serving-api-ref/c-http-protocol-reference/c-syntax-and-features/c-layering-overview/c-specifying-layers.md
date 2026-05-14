---
description: Nella sequenza di comandi dell'URL o del modificatore di catalogo, una sequenza di definizione del livello inizia con il comando layer= e termina con un altro comando layer=, un comando effect= o la fine dell'URL.
solution: Experience Manager
title: Specifica dei livelli
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
TQID: 'https://experienceleague.adobe.com/jNFpOYrBFWWc53JvzwENSjpM-SkIpenxxWPUgGX-p0Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 0%

---

# Specifica dei livelli{#specifying-layers}

Nella sequenza di comandi URL o catalog::Modifier, una sequenza di definizione di livello inizia con il comando layer= e termina con un altro comando layer=, un comando effect= o la fine dell&#39;URL.

Tutti i comandi all&#39;interno della sequenza di definizione del livello sono associati al livello.

Il comando `layer=` specifica un numero di livello, che deve essere un numero intero maggiore o uguale a 0. Tutti i comandi nelle sequenze di definizione dei livelli con lo stesso numero di livello vengono applicati allo stesso livello. Se lo stesso comando viene eseguito più di una volta, prevale l&#39;ultima istanza.
