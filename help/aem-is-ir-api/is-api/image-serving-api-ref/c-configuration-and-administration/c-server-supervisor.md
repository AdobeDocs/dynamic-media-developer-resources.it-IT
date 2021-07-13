---
description: I componenti Image Serving sono gestiti dal Server Supervisore, che è un daemon Linux o Windows Service (S7Supervisore.exe, elencato come 'Dynamic Media Image Serving' nel Pannello di controllo Campaign Servizi).
solution: Experience Manager
title: Supervisore server
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Supervisore server{#server-supervisor}

I componenti Image Serving sono gestiti dal Server Supervisore, che è un daemon Linux o Windows Service (S7Supervisore.exe, elencato come &#39;Dynamic Media Image Serving&#39; nel Pannello di controllo Campaign Servizi).

Oltre ad avviare e arrestare altri componenti di Image Serving, il Server Supervisore è responsabile di garantire lo stato di salute di questi altri componenti. In caso di arresto anomalo di un componente, questo viene riavviato automaticamente per ridurre al minimo le interruzioni del servizio.

## Avvio e arresto {#section-061d28d74e034a30adc39ea3e2031cd0}

Il supervisore del server viene avviato, arrestato e riavviato con lo script dell&#39;utilità Image Server. Per ulteriori informazioni, consulta la [Documentazione sulle utility](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) .

L&#39;avvio e l&#39;arresto automatico del Server Supervisore avvia e arresta tutti gli altri componenti di Image Server.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
