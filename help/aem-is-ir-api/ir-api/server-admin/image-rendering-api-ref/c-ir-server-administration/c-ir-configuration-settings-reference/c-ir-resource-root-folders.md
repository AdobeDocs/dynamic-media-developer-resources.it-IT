---
title: Cartelle principali delle risorse (ir.resourceRootPaths)
description: Un elenco di percorsi, delimitato da punti e virgola, funge da directory principali per tutti i file di dati con percorsi di file relativi.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
TQID: 'https://experienceleague.adobe.com/5mKCVHonfG4riWoIenUyFHtMnSg3cmL-Lm-YTGN34fA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 0%

---

# Cartelle principali delle risorse (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Un elenco di percorsi, delimitato da punti e virgola, funge da directory principali per tutti i file di dati con percorsi di file relativi.

Può essere un percorso assoluto o relativo a *[!DNL install_folder]*. Quando si specificano più percorsi, il server tenta ogni radice nell&#39;ordine specificato fino a quando il file non viene trovato. Il valore predefinito è [!DNL ./resources], per un percorso radice predefinito di [!DNL install_folder/resources].
