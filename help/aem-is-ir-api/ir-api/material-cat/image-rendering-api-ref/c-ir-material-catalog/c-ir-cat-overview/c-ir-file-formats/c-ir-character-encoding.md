---
title: Codifica dei caratteri
description: Immagine Rendering supporta cataloghi di materiali con codifica ISO-8859-1 e UTF-8.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Codifica dei caratteri{#character-encoding}

Immagine Rendering supporta cataloghi di materiali con codifica ISO-8859-1 e UTF-8.

Un byte order mark (BOM) viene utilizzato per specificare la codifica per ogni file. Per UTF-8, la distinta base è la sequenza `EF BB BF`di byte. La codifica UTF-8 viene assunta quando questa sequenza di caratteri viene rilevata all&#39;inizio di ogni file catalogo materiale. Qualsiasi altra sequenza di byte comporta l&#39;interpretazione del file come codificato secondo lo standard ISO-8859-1.

Molte applicazioni moderne, se configurate per UTF-8, inseriscono automaticamente la distinta base.
