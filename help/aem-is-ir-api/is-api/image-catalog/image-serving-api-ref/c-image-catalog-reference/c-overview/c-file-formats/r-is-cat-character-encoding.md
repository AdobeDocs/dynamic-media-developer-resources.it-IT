---
description: Image Serving supporta i cataloghi di immagini con codifica ISO-8859-1 e UTF-8.
seo-description: Image Serving supporta i cataloghi di immagini con codifica ISO-8859-1 e UTF-8.
seo-title: Codifica caratteri
solution: Experience Manager
title: Codifica caratteri
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Codifica caratteri{#character-encoding}

Image Serving supporta i cataloghi di immagini con codifica ISO-8859-1 e UTF-8.

Per specificare la codifica di ciascun file viene utilizzato un indicatore di ordine dei byte (BOM). Per UTF-8, la distinta base è la sequenza di byte `EF BB BF`. La codifica UTF-8 si presume quando questa sequenza di caratteri viene rilevata all&#39;inizio di ogni file di catalogo di immagini. Qualsiasi altra sequenza di byte fa sì che il file venga interpretato come codificato allo standard ISO-8859-1.

Molte applicazioni contemporanee, se configurate per UTF-8, inserisce automaticamente la distinta base.
