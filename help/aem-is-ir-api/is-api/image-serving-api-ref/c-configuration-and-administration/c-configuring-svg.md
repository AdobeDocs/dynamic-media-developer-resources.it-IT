---
description: Il componente SvgRender è un’applicazione Java indipendente.
solution: Experience Manager
title: Configurazione di SVG
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 2%

---


# Configurazione di SVG{#configuring-svg}

Il componente SvgRender è un’applicazione Java indipendente.

Le impostazioni di configurazione SVG si trovano in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] e [!DNL ServerSupervisorRegistry.xml].

Per comunicare tra SvgRender e Image Server viene utilizzata una connessione socket. Il numero di porta è 27346. Se necessario, può essere modificato impostando `SVGRender.port` in [!DNL svg.conf] e `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] su un nuovo valore.

## Consultate anche {#section-c085b47d54d44059bdaa67fd5e226e91}

[Impostazioni di configurazione SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
