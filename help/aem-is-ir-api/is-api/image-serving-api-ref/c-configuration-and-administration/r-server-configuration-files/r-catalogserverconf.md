---
description: Contiene le impostazioni relative alla gestione dei cataloghi di immagini.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# catalog-server.conf{#catalog-server-conf}

Contiene le impostazioni relative alla gestione dei cataloghi di immagini.

Questo file è un file di proprietà JAVA. Si deve fare attenzione a seguire le convenzioni appropriate; in caso contrario, l&#39;avvio del server Platform potrebbe non riuscire. Utilizzare una barra rovesciata doppia &#39;\\&#39; o una singola barra rovesciata &#39;/&#39; invece di una barra rovesciata &#39;\&#39; nei percorsi dei file di Windows. La barra rovesciata viene utilizzata come carattere di escape in questo tipo di file.

Le modifiche a questo file hanno effetto poco dopo il salvataggio del file.

Solo le impostazioni elencate di seguito possono essere modificate in [!DNL catalog-service.conf]. Se una particolare impostazione è assente, può essere aggiunta in qualsiasi punto del file. Può essere presente una sola istanza di ciascuna impostazione.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
