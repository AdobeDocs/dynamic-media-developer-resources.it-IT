---
description: Nella sequenza di comandi URL o modificatore catalogo, una sequenza di definizione del livello inizia con il comando layer= e termina con un altro comando layer=, un comando effect= o la fine dell’URL.
seo-description: Nella sequenza di comandi URL o modificatore catalogo, una sequenza di definizione del livello inizia con il comando layer= e termina con un altro comando layer=, un comando effect= o la fine dell’URL.
seo-title: Specifica dei livelli
solution: Experience Manager
title: Specifica dei livelli
topic: Scene7 Image Serving - Image Rendering API
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Specifica dei livelli{#specifying-layers}

Nella sequenza di comando URL o catalogo::Modificatore, una sequenza di definizione del livello inizia con il comando layer= e termina con un altro comando layer=, un comando effect= o la fine dell’URL.

Tutti i comandi nella sequenza di definizione del livello sono associati al livello.

Il `layer=` comando specifica un numero di livello, che deve essere un numero intero pari o superiore a 0. Tutti i comandi nelle sequenze di definizione del livello con lo stesso numero di livello vengono applicati allo stesso livello. Se lo stesso comando si verifica più volte, prevarrà l&#39;ultima istanza.
