---
description: I file di dati dell'origine di contenuto statico sono accessibili solo da  [!DNL Platform Server].
solution: Experience Manager
title: Dati origine di contenuto statico
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
TQID: 'https://experienceleague.adobe.com/XFhKuqGPsarkFZcYcBo7XuyCEsiJINf-o6koIZQKAXU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# Dati origine di contenuto statico{#static-content-source-data}

I file di dati dell&#39;origine di contenuto statico sono accessibili solo da [!DNL Platform Server].

Il percorso dei file di dati di contenuto statico viene risolto come segue:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Il server combina i segmenti di percorso da destra a sinistra fino a quando non viene stabilito un percorso di file assoluto.

Tutti i ` *[!DNL rootPath]*` segmenti possono essere vuoti, relativi o assoluti.

` *[!DNL catalogPath]*` è un nome o un percorso di file assoluto o relativo. *[!DNL requestPath]* deve essere un nome o un percorso di file relativo.

È possibile definire più valori `PS::staticContent.rootPaths` in [!DNL PlatformServer.conf]. Questo consente di distribuire i file di dati di origine su più file system. [!DNL Platform Server] tenta percorsi alternativi nell&#39;ordine specificato finché non viene trovato il file di dati.
