---
description: Il componente SvgRender è un’applicazione Java indipendente.
seo-description: Il componente SvgRender è un’applicazione Java indipendente.
seo-title: Configurazione di SVG
solution: Experience Manager
title: Configurazione di SVG
uuid: f6e131af-283e-4649-b349-123489c0838d
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 2%

---


# Configurazione di SVG{#configuring-svg}

Il componente SvgRender è un’applicazione Java indipendente.

Le impostazioni di configurazione SVG si trovano in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] e [!DNL ServerSupervisorRegistry.xml].

Per comunicare tra SvgRender e Image Server viene utilizzata una connessione socket. Il numero di porta è 27346. Se necessario, può essere modificato impostando `SVGRender.port` in [!DNL svg.conf] e `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] su un nuovo valore.

## Consultate anche {#section-c085b47d54d44059bdaa67fd5e226e91}

[Impostazioni di configurazione SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
