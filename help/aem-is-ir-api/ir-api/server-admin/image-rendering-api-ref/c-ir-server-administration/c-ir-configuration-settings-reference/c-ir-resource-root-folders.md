---
description: Elenco di percorsi, delimitati da punti e virgola, fungono da radice per tutti i file di dati con percorsi di file relativi.
solution: Experience Manager
title: Cartelle radice delle risorse (ir.resourceRootPaths)
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# Cartelle radice delle risorse (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Elenco di percorsi, delimitati da punti e virgola, fungono da radice per tutti i file di dati con percorsi di file relativi.

Possono essere percorsi assoluti o percorsi relativi a *[!DNL install_folder]*. Quando vengono specificati più percorsi, il server proverà ogni radice nell&#39;ordine specificato fino a quando il file non viene trovato. Il valore predefinito è [!DNL ./resources], per un percorso principale predefinito di [!DNL install_folder/resources].
