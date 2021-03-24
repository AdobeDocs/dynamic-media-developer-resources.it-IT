---
description: Elenco di percorsi, delimitati da punti e virgola, fungono da radice per tutti i file di dati con percorsi di file relativi.
solution: Experience Manager
title: Cartelle radice delle risorse (ir.resourceRootPaths)
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Cartelle radice delle risorse (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Elenco di percorsi, delimitati da punti e virgola, fungono da radice per tutti i file di dati con percorsi di file relativi.

Possono essere percorsi assoluti o percorsi relativi a *[!DNL install_folder]*. Quando vengono specificati più percorsi, il server proverà ogni radice nell&#39;ordine specificato fino a quando il file non viene trovato. Il valore predefinito è [!DNL ./resources], per un percorso principale predefinito di [!DNL install_folder/resources].
