---
description: Le impostazioni di configurazione Image Rendering sono memorizzate nel file di configurazione Platform Server.
seo-description: Le impostazioni di configurazione Image Rendering sono memorizzate nel file di configurazione Platform Server.
seo-title: File di configurazione
solution: Experience Manager
title: File di configurazione
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# File di configurazione{#configuration-files}

Le impostazioni di configurazione Image Rendering sono memorizzate nel file di configurazione Platform Server.

Il file di configurazione del server della piattaforma si trova in [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Questo file è un file di proprietà JAVA. È necessario prestare attenzione a seguire le convenzioni appropriate, altrimenti Platform Server potrebbe non avviarsi. Nei percorsi dei file Windows deve essere utilizzata una barra rovesciata doppia (`\\`) o una singola barra rovesciata (/) invece di una barra rovesciata semplice (\), in quanto la barra rovesciata viene utilizzata come carattere di escape in questo tipo di file. Il file contiene proprietà non documentate che sono per uso interno del server e non devono essere modificate.

Per un elenco di tutte le impostazioni di configurazione Image Rendering, fare riferimento a [Riferimento impostazioni di configurazione](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81).
