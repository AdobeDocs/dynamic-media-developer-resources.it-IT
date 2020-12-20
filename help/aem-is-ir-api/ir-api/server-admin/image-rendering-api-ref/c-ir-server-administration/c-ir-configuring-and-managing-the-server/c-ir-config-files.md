---
description: Le impostazioni di configurazione del rendering delle immagini sono memorizzate nel file di configurazione del server della piattaforma.
seo-description: Le impostazioni di configurazione del rendering delle immagini sono memorizzate nel file di configurazione del server della piattaforma.
seo-title: File di configurazione
solution: Experience Manager
title: File di configurazione
topic: Scene7 Image Serving - Image Rendering API
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# File di configurazione{#configuration-files}

Le impostazioni di configurazione del rendering delle immagini sono memorizzate nel file di configurazione del server della piattaforma.

Il file di configurazione del server della piattaforma si trova in [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Questo file è un file di proprietà JAVA. Prestate attenzione a seguire le convenzioni appropriate, in caso contrario il server della piattaforma potrebbe non avviarsi. Nei percorsi dei file Windows deve essere utilizzata una doppia barra rovesciata (`\\`) o una singola barra rovesciata (/), invece di una semplice barra rovesciata (\), in quanto la barra rovesciata viene utilizzata come carattere di escape in questo tipo di file. Il file contiene proprietà non documentate, che sono per uso interno del server e non devono essere modificate.

Per un elenco di tutte le impostazioni di configurazione del rendering delle immagini, fare riferimento alla [Guida di riferimento delle impostazioni di configurazione](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81).
