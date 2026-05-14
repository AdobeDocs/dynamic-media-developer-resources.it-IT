---
description: I componenti Image Server sono gestiti dal Supervisore server, che è un daemon Linux o un servizio Windows (S7Supervisor.exe, elencato come 'Dynamic Media Image Server' nel Pannello di controllo Campaign Services).
solution: Experience Manager
title: Supervisore server
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
TQID: 'https://experienceleague.adobe.com/D3cGGQLVly7MwWSvSjkWcWkuR9kVUFC9sSvItZm6eOc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# Supervisore server{#server-supervisor}

I componenti Image Server sono gestiti dal Supervisore server, che è un daemon Linux o un servizio Windows (S7Supervisor.exe, elencato come &#39;Dynamic Media Image Server&#39; nel Pannello di controllo Campaign Services).

Oltre ad avviare e arrestare altri componenti di Image Server, il Supervisore server è responsabile della loro integrità. In caso di arresto anomalo di un componente, questo viene riavviato automaticamente per ridurre al minimo le interruzioni del servizio.

## Avvio e arresto {#section-061d28d74e034a30adc39ea3e2031cd0}

Il Server Supervisor viene avviato, arrestato e riavviato con lo script dell&#39;utilità Image Server. Per ulteriori informazioni, consulta la [documentazione sulle utilità](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f).

L&#39;avvio e l&#39;arresto di Server Supervisor determinano l&#39;avvio e l&#39;arresto automatici di tutti gli altri componenti di Image Server.

[RegistroSupervisore.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
