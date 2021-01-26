---
description: Contiene impostazioni relative alla gestione dei cataloghi di immagini.
seo-description: Contiene impostazioni relative alla gestione dei cataloghi di immagini.
seo-title: catalog-server.conf
solution: Experience Manager
title: catalog-server.conf
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 797a43d2-18f5-4735-8b19-da231952b1a2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# catalog-server.conf{#catalog-server-conf}

Contiene impostazioni relative alla gestione dei cataloghi di immagini.

Questo file è un file di proprietà JAVA. Occorre fare attenzione a seguire le convenzioni appropriate; in caso contrario, il server della piattaforma potrebbe non avviarsi. Nei percorsi dei file Windows, utilizzate una doppia barra rovesciata &#39;\\&#39; o una singola barra rovesciata &#39;/&#39; invece di una barra rovesciata &#39;\&#39;. La barra rovesciata viene utilizzata come carattere di escape in questo tipo di file.

Le modifiche a questo file hanno effetto poco dopo il salvataggio del file.

Solo le impostazioni elencate di seguito possono essere modificate in [!DNL catalog-service.conf]. Se una particolare impostazione è assente, può essere aggiunta ovunque nel file. Può essere presente una sola istanza di ciascuna impostazione.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
