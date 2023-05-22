---
description: I componenti Image Server sono gestiti dal Supervisore server, che è un daemon Linux o un servizio Windows (S7Supervisor.exe, elencato come 'Dynamic Media Image Server' nel Pannello di controllo Campaign Servizi).
solution: Experience Manager
title: Supervisore server
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Supervisore server{#server-supervisor}

I componenti Image Server sono gestiti dal Supervisore server, che è un daemon Linux o un servizio Windows (S7Supervisor.exe, elencato come &#39;Dynamic Media Image Server&#39; nel Pannello di controllo Campaign Servizi).

Oltre ad avviare e arrestare altri componenti di Image Server, il Supervisore server è responsabile della loro integrità. In caso di arresto anomalo di un componente, questo viene riavviato automaticamente per ridurre al minimo le interruzioni del servizio.

## Avvio e arresto {#section-061d28d74e034a30adc39ea3e2031cd0}

Il Server Supervisor viene avviato, arrestato e riavviato con lo script dell&#39;utilità Image Server. Consulta la [Documentazione sulle utilità](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) per ulteriori informazioni.

L&#39;avvio e l&#39;arresto di Server Supervisor determinano l&#39;avvio e l&#39;arresto automatici di tutti gli altri componenti di Image Server.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
