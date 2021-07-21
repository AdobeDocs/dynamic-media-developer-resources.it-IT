---
description: Le impostazioni di configurazione Image Rendering sono memorizzate nel file di configurazione Platform Server.
solution: Experience Manager
title: File di configurazione
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# File di configurazione{#configuration-files}

Le impostazioni di configurazione Image Rendering sono memorizzate nel file di configurazione Platform Server.

Il file di configurazione del server della piattaforma si trova in [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Questo file è un file di proprietà JAVA. È necessario prestare attenzione a seguire le convenzioni appropriate, altrimenti Platform Server potrebbe non avviarsi. Nei percorsi dei file Windows deve essere utilizzata una barra rovesciata doppia (`\\`) o una singola barra rovesciata (/) invece di una barra rovesciata semplice (\), in quanto la barra rovesciata viene utilizzata come carattere di escape in questo tipo di file. Il file contiene proprietà non documentate che sono per uso interno del server e non devono essere modificate.

Per un elenco di tutte le impostazioni di configurazione Image Rendering, fare riferimento a [Riferimento impostazioni di configurazione](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81).
