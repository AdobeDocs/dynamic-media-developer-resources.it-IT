---
description: I file di dati di origine del contenuto statico sono accessibili solo dal server piattaforma.
seo-description: I file di dati di origine del contenuto statico sono accessibili solo dal server piattaforma.
seo-title: Dati origine contenuto statico
solution: Experience Manager
title: Dati origine contenuto statico
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# Dati origine contenuto statico{#static-content-source-data}

I file di dati di origine del contenuto statico sono accessibili solo dal server piattaforma.

Il percorso dei file di dati di contenuto statico è stato risolto come segue:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Il server combina i segmenti di percorso da destra a sinistra finché non viene definito un percorso di file assoluto.

Tutti i segmenti ` *[!DNL rootPath]*` possono essere vuoti, relativi o assoluti.

` *[!DNL catalogPath]*` è un nome/percorso di file assoluto o relativo. *[!DNL requestPath]* deve essere un percorso/nome di file relativo.

Più valori `PS::staticContent.rootPaths` possono essere definiti in [!DNL PlatformServer.conf]. Questo consente la distribuzione dei file di dati di origine tra più file system. Il server piattaforme proverà percorsi alternativi nell&#39;ordine specificato fino a trovare il file di dati.
