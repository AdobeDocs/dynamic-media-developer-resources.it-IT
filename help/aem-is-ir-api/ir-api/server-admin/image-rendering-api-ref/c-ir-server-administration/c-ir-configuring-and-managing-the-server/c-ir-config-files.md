---
description: Le impostazioni di configurazione di Image Rendering sono memorizzate nel file di configurazione  [!DNL Platform Server] .
solution: Experience Manager
title: File di configurazione
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
TQID: 'https://experienceleague.adobe.com/KTBXtuSOstPMi7bPQg70jyUVCqcXlLiLPiFFhyp9iFg'
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
source-wordcount: 122
ht-degree: 0%

---

# File di configurazione{#configuration-files}

Le impostazioni di configurazione di Image Rendering sono memorizzate nel file di configurazione [!DNL Platform Server].

Il file di configurazione del server di piattaforma si trova in [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Questo file è un file di proprietà JAVA. Fare attenzione a seguire le convenzioni appropriate, altrimenti l&#39;avvio di [!DNL Platform Server] potrebbe non riuscire. È necessario utilizzare una doppia barra rovesciata (`\\`) o una singola barra (/) invece di una semplice barra rovesciata (\) nei percorsi dei file di Windows, perché la barra rovesciata viene utilizzata come carattere di escape in questo tipo di file. Il file contiene proprietà non documentate, che sono destinate all’uso interno del server e non devono essere modificate.

Per un elenco di tutte le impostazioni di configurazione di Image Rendering, fare riferimento alla [documentazione sulle impostazioni di configurazione](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81).
