---
description: Image Serving supporta i cataloghi di immagini con codifica ISO-8859-1 e UTF-8.
solution: Experience Manager
title: Codifica caratteri
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Codifica caratteri{#character-encoding}

Image Serving supporta i cataloghi di immagini con codifica ISO-8859-1 e UTF-8.

Per specificare la codifica di ciascun file viene utilizzato un indicatore di ordine dei byte (BOM). Per UTF-8, la distinta base è la sequenza di byte `EF BB BF`. La codifica UTF-8 si presume quando questa sequenza di caratteri viene rilevata all&#39;inizio di ogni file di catalogo di immagini. Qualsiasi altra sequenza di byte fa sì che il file venga interpretato come codificato allo standard ISO-8859-1.

Molte applicazioni contemporanee, se configurate per UTF-8, inserisce automaticamente la distinta base.
