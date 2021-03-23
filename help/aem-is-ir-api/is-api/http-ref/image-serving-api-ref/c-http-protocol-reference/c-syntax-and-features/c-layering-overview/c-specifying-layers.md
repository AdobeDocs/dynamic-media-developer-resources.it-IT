---
description: Nella sequenza di comando modificatore URL o catalogo, una sequenza di definizione del livello inizia con il comando layer= e termina con un altro comando layer= , un comando effect= o la fine dell'URL.
seo-description: Nella sequenza di comando modificatore URL o catalogo, una sequenza di definizione del livello inizia con il comando layer= e termina con un altro comando layer= , un comando effect= o la fine dell'URL.
seo-title: Specifica dei livelli
solution: Experience Manager
title: Specifica dei livelli
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# Specifica dei livelli{#specifying-layers}

Nella sequenza di comando URL o catalog::Modifier, una sequenza di definizione del livello inizia con il comando layer= e termina con un altro comando layer=, un comando effect= o la fine dell&#39;URL.

Tutti i comandi della sequenza di definizione del livello sono associati al livello.

Il comando `layer=` specifica un numero di livello, che deve essere un numero intero pari a 0 o superiore. Tutti i comandi nelle sequenze di definizione del livello con lo stesso numero di livello vengono applicati allo stesso livello. Se lo stesso comando si verifica più di una volta, prevale l&#39;ultima istanza.
