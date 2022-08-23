---
title: Codifica caratteri
description: Image Rendering supporta cataloghi di materiali con codifica ISO-8859-1 e UTF-8.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Codifica caratteri{#character-encoding}

Image Rendering supporta cataloghi di materiali con codifica ISO-8859-1 e UTF-8.

Per specificare la codifica di ciascun file viene utilizzato un indicatore di ordine dei byte (BOM). Per UTF-8, la distinta base è la sequenza di byte `EF BB BF`. La codifica UTF-8 si presume quando questa sequenza di caratteri viene rilevata all&#39;inizio di ogni file di catalogo del materiale. Qualsiasi altra sequenza di byte fa sì che il file venga interpretato come codificato allo standard ISO-8859-1.

Molte applicazioni contemporanee, se configurate per UTF-8, inseriscono automaticamente la distinta base.
