---
description: Il componente SvgRender è un’applicazione Java indipendente.
seo-description: Il componente SvgRender è un’applicazione Java indipendente.
seo-title: Configurazione di SVG
solution: Experience Manager
title: Configurazione di SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: f6e131af-283e-4649-b349-123489c0838d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Configurazione di SVG{#configuring-svg}

Il componente SvgRender è un’applicazione Java indipendente.

Le impostazioni di configurazione SVG si trovano in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml]e [!DNL ServerSupervisorRegistry.xml].

Una connessione socket viene utilizzata per comunicare tra SvgRender e il server immagini. Il numero della porta è 27346. Se necessario, può essere modificato impostando `SVGRender.port` in e [!DNL svg.conf] in `<SVGTcpPort>` [!DNL ImageServerRegistry.xml] un nuovo valore.

## Consultate anche {#section-c085b47d54d44059bdaa67fd5e226e91}

[Impostazioni di configurazione SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
