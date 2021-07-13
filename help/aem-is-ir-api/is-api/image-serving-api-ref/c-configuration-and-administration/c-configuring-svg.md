---
description: Il componente SvgRender è un’applicazione Java indipendente.
solution: Experience Manager
title: Configurazione di SVG
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# Configurazione di SVG{#configuring-svg}

Il componente SvgRender è un’applicazione Java indipendente.

Le impostazioni di configurazione SVG si trovano in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] e [!DNL ServerSupervisorRegistry.xml].

Per comunicare tra SvgRender e Image Server viene utilizzata una connessione socket. Il numero di porta è 27346. Se necessario, può essere modificato impostando `SVGRender.port` in [!DNL svg.conf] e `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] su un nuovo valore.

## Consultate anche {#section-c085b47d54d44059bdaa67fd5e226e91}

[Impostazioni di configurazione SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
