---
description: I componenti Image Server sono gestiti dal Server Supervisore, che è un demone Linux o Windows Service (S7Supervisore.exe, elencato come 'Scene7 Image Server' nel Pannello di controllo Campaign Servizi).
seo-description: I componenti Image Server sono gestiti dal Server Supervisore, che è un demone Linux o Windows Service (S7Supervisore.exe, elencato come 'Scene7 Image Server' nel Pannello di controllo Campaign Servizi).
seo-title: Supervisore server
solution: Experience Manager
title: Supervisore server
topic: Scene7 Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Supervisore server{#server-supervisor}

I componenti Image Server sono gestiti dal Server Supervisore, che è un demone Linux o Windows Service (S7Supervisore.exe, elencato come &#39;Scene7 Image Server&#39; nel Pannello di controllo Campaign Servizi).

Oltre ad avviare e arrestare altri componenti Image Server, il Server Supervisore è responsabile della protezione dello stato di salute di questi altri componenti. In caso di arresto anomalo di un componente, questo viene riavviato automaticamente per ridurre al minimo le interruzioni del servizio.

## Avvio e arresto di {#section-061d28d74e034a30adc39ea3e2031cd0}

Il supervisore del server viene avviato, arrestato e riavviato con lo script dell&#39;utilità Image Server. Per ulteriori informazioni, consultare la [Documentazione sulle utility](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f).

L’avvio e l’arresto di Server Supervisore avviano e arrestano automaticamente tutti gli altri componenti di Image Server.

[SupervisoreRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
