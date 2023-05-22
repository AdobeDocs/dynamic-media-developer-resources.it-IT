---
description: L’elenco dei percorsi, delimitato da punti e virgola, funge da directory principali per tutti i file di dati con percorsi di file relativi.
solution: Experience Manager
title: Cartelle principali delle risorse (ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# Cartelle principali delle risorse (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

L’elenco dei percorsi, delimitato da punti e virgola, funge da directory principali per tutti i file di dati con percorsi di file relativi.

Possono essere percorsi assoluti o relativi a *[!DNL install_folder]*. Quando vengono specificati più percorsi, il server tenterà ogni radice nell&#39;ordine specificato fino a quando il file non viene trovato. Il valore predefinito è [!DNL ./resources], per un percorso directory principale predefinito di [!DNL install_folder/resources].
