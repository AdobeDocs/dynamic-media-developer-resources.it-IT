---
description: Image Rendering supporta cataloghi di materiali con codifica ISO-8859-1 e UTF-8.
seo-description: Image Rendering supporta cataloghi di materiali con codifica ISO-8859-1 e UTF-8.
seo-title: Codifica caratteri
solution: Experience Manager
title: Codifica caratteri
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Codifica caratteri{#character-encoding}

Image Rendering supporta cataloghi di materiali con codifica ISO-8859-1 e UTF-8.

Per specificare la codifica di ciascun file viene utilizzato un indicatore di ordine dei byte (BOM). Per UTF-8, la distinta base è la sequenza di byte `EF BB BF`. La codifica UTF-8 si presume quando questa sequenza di caratteri viene rilevata all&#39;inizio di ogni file di catalogo del materiale. Qualsiasi altra sequenza di byte fa sì che il file venga interpretato come codificato allo standard ISO-8859-1.

Molte applicazioni contemporanee, se configurate per UTF-8, inseriscono automaticamente la distinta base.
