---
description: I file di dati di origine del contenuto statico sono accessibili solo da Platform Server.
solution: Experience Manager
title: Dati origine contenuto statici
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Dati origine contenuto statici{#static-content-source-data}

I file di dati di origine del contenuto statico sono accessibili solo da Platform Server.

Il percorso dei file di dati di contenuto statico viene risolto come segue:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Il server combina i segmenti di percorso da destra a sinistra fino a quando non viene stabilito un percorso di file assoluto.

Tutti i segmenti ` *[!DNL rootPath]*` possono essere vuoti, relativi o assoluti.

` *[!DNL catalogPath]*` è un percorso/nome file assoluto o relativo. *[!DNL requestPath]* deve essere un percorso/nome file relativo.

È possibile definire più valori `PS::staticContent.rootPaths` in [!DNL PlatformServer.conf]. Ciò consente la distribuzione dei file di dati di origine su più file system. Platform Server proverà percorsi alternativi nell’ordine specificato fino a quando non viene trovato il file di dati.
