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

Questo file è un file di proprietà JAVA. Si deve fare attenzione a seguire le convenzioni appropriate; altrimenti [!DNL Platform Server] potrebbero non avviarsi. Utilizzare una barra rovesciata doppia &#39;\\&#39; o una singola barra rovesciata &#39;/&#39; invece di una barra rovesciata &#39;\&#39; nei percorsi dei file di Windows. La barra rovesciata viene utilizzata come carattere di escape in questo tipo di file.

Le modifiche a questo file hanno effetto poco dopo il salvataggio del file.

È possibile modificare solo le impostazioni elencate di seguito in [!DNL catalog-service.conf]. Se una particolare impostazione è assente, può essere aggiunta in qualsiasi punto del file. Può essere presente una sola istanza di ciascuna impostazione.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
