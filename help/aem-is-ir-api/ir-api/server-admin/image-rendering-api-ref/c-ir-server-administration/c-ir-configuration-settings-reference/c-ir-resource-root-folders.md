---
title: Cartelle principali delle risorse (ir.resourceRootPaths)
description: Un elenco di percorsi, delimitato da punti e virgola, funge da directory principali per tutti i file di dati con percorsi di file relativi.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# Cartelle principali delle risorse (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Un elenco di percorsi, delimitato da punti e virgola, funge da directory principali per tutti i file di dati con percorsi di file relativi.

Può essere un percorso assoluto o relativo a *[!DNL install_folder]*. Quando si specificano più percorsi, il server tenta ogni radice nell&#39;ordine specificato fino a quando il file non viene trovato. Il valore predefinito è [!DNL ./resources], per un percorso radice predefinito di [!DNL install_folder/resources].
