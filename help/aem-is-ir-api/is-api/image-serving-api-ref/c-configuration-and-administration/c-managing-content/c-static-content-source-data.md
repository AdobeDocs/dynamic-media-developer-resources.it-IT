---
description: I file di dati di origine del contenuto statico sono accessibili solo dal [!DNL Platform Server].
solution: Experience Manager
title: Dati origine contenuto statici
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Dati origine contenuto statici{#static-content-source-data}

I file di dati di origine del contenuto statico sono accessibili solo dal [!DNL Platform Server].

Il percorso dei file di dati di contenuto statico viene risolto come segue:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Il server combina i segmenti di percorso da destra a sinistra fino a quando non viene stabilito un percorso di file assoluto.

Tutto ` *[!DNL rootPath]*` i segmenti possono essere vuoti, relativi o assoluti.

` *[!DNL catalogPath]*` è un percorso/nome file assoluto o relativo. *[!DNL requestPath]* deve essere un percorso/nome file relativo.

Multipli `PS::staticContent.rootPaths` possono essere definiti in [!DNL PlatformServer.conf]. Ciò consente la distribuzione dei file di dati di origine su più file system. La [!DNL Platform Server] proveranno percorsi alternativi nell&#39;ordine specificato fino a quando il file di dati non viene trovato.
