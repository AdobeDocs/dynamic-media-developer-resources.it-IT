---
description: Le impostazioni di configurazione del rendering delle immagini sono memorizzate in [!DNL Platform Server] file di configurazione.
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

Le impostazioni di configurazione del rendering delle immagini sono memorizzate in [!DNL Platform Server] file di configurazione.

Il file di configurazione del server della piattaforma si trova in [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Questo file è un file di proprietà JAVA. Occorre fare attenzione a seguire le convenzioni appropriate, altrimenti la [!DNL Platform Server] potrebbe non riuscire ad avviarsi. Una barra rovesciata doppia (`\\`) o una singola barra (/) deve essere utilizzata al posto di una barra rovesciata semplice (\) nei percorsi dei file di Windows, perché la barra rovesciata viene utilizzata come carattere di escape in questo tipo di file. Il file contiene proprietà non documentate che sono per uso interno del server e non devono essere modificate.

Fai riferimento a [Riferimento per le impostazioni di configurazione](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) per un elenco di tutte le impostazioni di configurazione Image Rendering.
