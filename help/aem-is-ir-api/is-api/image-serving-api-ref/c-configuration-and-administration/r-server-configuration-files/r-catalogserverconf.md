---
description: Contiene le impostazioni relative alla gestione dei cataloghi di immagini.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
TQID: 'https://experienceleague.adobe.com/GdtVY3WMO9F6C5vzkOHdVoMW-f6-L1cJGUt1KUCvLJ8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
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
