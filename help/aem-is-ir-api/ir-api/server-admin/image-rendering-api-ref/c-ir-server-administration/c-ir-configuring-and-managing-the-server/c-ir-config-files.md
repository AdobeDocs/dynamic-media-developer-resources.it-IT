---
description: Le impostazioni di configurazione di Image Rendering sono memorizzate nel file di configurazione  [!DNL Platform Server] .
solution: Experience Manager
title: File di configurazione
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# File di configurazione{#configuration-files}

Le impostazioni di configurazione di Image Rendering sono memorizzate nel file di configurazione [!DNL Platform Server].

Il file di configurazione del server di piattaforma si trova in [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Questo file è un file di proprietà JAVA. Fare attenzione a seguire le convenzioni appropriate, altrimenti l&#39;avvio di [!DNL Platform Server] potrebbe non riuscire. È necessario utilizzare una doppia barra rovesciata (`\\`) o una singola barra (/) invece di una semplice barra rovesciata (\) nei percorsi dei file di Windows, perché la barra rovesciata viene utilizzata come carattere di escape in questo tipo di file. Il file contiene proprietà non documentate, che sono destinate all’uso interno del server e non devono essere modificate.

Per un elenco di tutte le impostazioni di configurazione di Image Rendering, fare riferimento alla [documentazione sulle impostazioni di configurazione](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81).
