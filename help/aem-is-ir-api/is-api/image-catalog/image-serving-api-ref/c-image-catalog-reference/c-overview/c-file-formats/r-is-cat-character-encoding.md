---
description: Image Server supporta cataloghi di immagini con codifica ISO-8859-1 e UTF-8.
solution: Experience Manager
title: Codifica caratteri
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
TQID: 'https://experienceleague.adobe.com/tsIJu-zCT-NlV6SD1I1pPYQ0DfqNcu9jSCBVXCcQ9tE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# Codifica caratteri{#character-encoding}

Image Server supporta cataloghi di immagini con codifica ISO-8859-1 e UTF-8.

Per specificare la codifica per ciascun file viene utilizzato un indicatore di ordine dei byte (BOM, Byte Order Mark). Per UTF-8, la distinta base è la sequenza di byte `EF BB BF`. Si presume la codifica UTF-8 quando questa sequenza di caratteri viene rilevata all&#39;inizio di ogni file di catalogo delle immagini. Qualsiasi altra sequenza di byte fa sì che il file venga interpretato come codificato nello standard ISO-8859-1.

Molte applicazioni contemporanee, se configurate per UTF-8, inseriscono automaticamente la distinta base.
