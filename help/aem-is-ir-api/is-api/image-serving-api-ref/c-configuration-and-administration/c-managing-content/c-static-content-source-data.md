---
description: I file di dati dell'origine di contenuto statico sono accessibili solo da [!DNL Platform Server].
solution: Experience Manager
title: Dati origine di contenuto statico
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Dati origine di contenuto statico{#static-content-source-data}

I file di dati dell&#39;origine di contenuto statico sono accessibili solo da [!DNL Platform Server].

Il percorso dei file di dati di contenuto statico viene risolto come segue:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Il server combina i segmenti di percorso da destra a sinistra fino a quando non viene stabilito un percorso di file assoluto.

Tutti ` *[!DNL rootPath]*` i segmenti possono essere vuoti, relativi o assoluti.

` *[!DNL catalogPath]*` è un nome o un percorso di file assoluto o relativo. *[!DNL requestPath]* deve essere un percorso/nome file relativo.

Più `PS::staticContent.rootPaths` i valori possono essere definiti in [!DNL PlatformServer.conf]. Questo consente di distribuire i file di dati di origine su più file system. Il [!DNL Platform Server] tenta percorsi alternativi nell’ordine specificato fino a quando non viene trovato il file di dati.
