---
description: Il componente SvgRender è un'applicazione Java indipendente.
solution: Experience Manager
title: Configurazione di SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 3%

---

# Configurazione di SVG{#configuring-svg}

Il componente SvgRender è un&#39;applicazione Java indipendente.

Le impostazioni di configurazione di SVG si trovano in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] e [!DNL ServerSupervisorRegistry.xml].

Una connessione socket viene utilizzata per comunicare tra SvgRender e il server immagini. Numero di porta 27346. Se necessario, è possibile modificarlo impostando `SVGRender.port` in [!DNL svg.conf] e `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] su un nuovo valore.

## Consultate anche {#section-c085b47d54d44059bdaa67fd5e226e91}

[Impostazioni configurazione SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
