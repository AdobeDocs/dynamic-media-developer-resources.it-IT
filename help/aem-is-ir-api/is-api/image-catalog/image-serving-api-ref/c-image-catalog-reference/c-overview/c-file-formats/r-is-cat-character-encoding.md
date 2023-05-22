---
description: Image Server supporta cataloghi di immagini con codifica ISO-8859-1 e UTF-8.
solution: Experience Manager
title: Codifica caratteri
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Codifica caratteri{#character-encoding}

Image Server supporta cataloghi di immagini con codifica ISO-8859-1 e UTF-8.

Per specificare la codifica per ciascun file viene utilizzato un indicatore di ordine dei byte (BOM, Byte Order Mark). Per UTF-8, la distinta base è la sequenza di byte `EF BB BF`. Si presume la codifica UTF-8 quando questa sequenza di caratteri viene rilevata all&#39;inizio di ogni file di catalogo delle immagini. Qualsiasi altra sequenza di byte fa sì che il file venga interpretato come codificato nello standard ISO-8859-1.

Molte applicazioni contemporanee, se configurate per UTF-8, inseriscono automaticamente la distinta base.
