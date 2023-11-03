---
description: Nella sequenza di comandi dell'URL o del modificatore di catalogo, una sequenza di definizione del livello inizia con il comando layer= e termina con un altro comando layer=, un comando effect= o la fine dell'URL.
solution: Experience Manager
title: Specifica dei livelli
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Specifica dei livelli{#specifying-layers}

Nella sequenza di comandi URL o catalog::Modifier, una sequenza di definizione di livello inizia con il comando layer= e termina con un altro comando layer=, un comando effect= o la fine dell&#39;URL.

Tutti i comandi all&#39;interno della sequenza di definizione del livello sono associati al livello.

Il `layer=` comando specifica un numero di livello, che deve essere un numero intero uguale o maggiore di 0. Tutti i comandi nelle sequenze di definizione dei livelli con lo stesso numero di livello vengono applicati allo stesso livello. Se lo stesso comando viene eseguito più di una volta, prevale l&#39;ultima istanza.
