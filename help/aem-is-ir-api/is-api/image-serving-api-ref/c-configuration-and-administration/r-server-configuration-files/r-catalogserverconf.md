---
description: Contiene le impostazioni relative alla gestione dei cataloghi di immagini.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

Contiene le impostazioni relative alla gestione dei cataloghi di immagini.

Questo file è un file di proprietà JAVA. Fare attenzione a seguire le convenzioni appropriate. In caso contrario, [!DNL Platform Server] potrebbe non essere avviato. Utilizzare una doppia barra rovesciata &#39;\\&#39; o una singola barra in avanti &#39;/&#39; invece della barra rovesciata &#39;\&#39; nei percorsi dei file di Windows. La barra rovesciata viene utilizzata come carattere di escape in questo tipo di file.

Le modifiche apportate al file hanno effetto poco dopo il salvataggio.

Solo le impostazioni elencate di seguito possono essere modificate in [!DNL catalog-service.conf]. Se una particolare impostazione è assente, può essere aggiunta ovunque nel file. È possibile che sia presente una sola istanza di ciascuna impostazione.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
