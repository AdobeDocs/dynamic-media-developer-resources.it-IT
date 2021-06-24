---
description: Nella sequenza di comando modificatore URL o catalogo, una sequenza di definizione del livello inizia con il comando layer= e termina con un altro comando layer= , un comando effect= o la fine dell'URL.
solution: Experience Manager
title: Specifica dei livelli
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Specifica dei livelli{#specifying-layers}

Nella sequenza di comando URL o catalog::Modifier, una sequenza di definizione del livello inizia con il comando layer= e termina con un altro comando layer=, un comando effect= o la fine dell&#39;URL.

Tutti i comandi della sequenza di definizione del livello sono associati al livello.

Il comando `layer=` specifica un numero di livello, che deve essere un numero intero pari a 0 o superiore. Tutti i comandi nelle sequenze di definizione del livello con lo stesso numero di livello vengono applicati allo stesso livello. Se lo stesso comando si verifica più di una volta, prevale l&#39;ultima istanza.
