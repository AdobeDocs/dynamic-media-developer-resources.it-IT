---
description: Image Rendering supporta cataloghi di materiali con codifica ISO-8859-1 e UTF-8.
seo-description: Image Rendering supporta cataloghi di materiali con codifica ISO-8859-1 e UTF-8.
seo-title: Codifica dei caratteri
solution: Experience Manager
title: Codifica dei caratteri
topic: Scene7 Image Serving - Image Rendering API
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Codifica caratteri{#character-encoding}

Image Rendering supporta cataloghi di materiali con codifica ISO-8859-1 e UTF-8.

Per specificare la codifica di ciascun file viene utilizzato un indicatore di ordine byte (BOM). Per UTF-8, la distinta base è la sequenza di byte `EF BB BF`. La codifica UTF-8 viene utilizzata quando questa sequenza di caratteri viene rilevata all&#39;inizio di ciascun file catalogo di materiali. Qualsiasi altra sequenza di byte fa sì che il file venga interpretato come codificato nello standard ISO-8859-1.

Molte applicazioni contemporanee, se configurate per UTF-8, inseriscono automaticamente la distinta base.
