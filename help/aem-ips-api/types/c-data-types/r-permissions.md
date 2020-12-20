---
description: Gestisce i diritti di accesso, modifica, creazione o eliminazione delle risorse per gruppo.
seo-description: Gestisce i diritti di accesso, modifica, creazione o eliminazione delle risorse per gruppo.
seo-title: Autorizzazione
solution: Experience Manager
title: Autorizzazione
topic: Scene7 Image Production System API
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 6%

---


# Permission{#permission}

Gestisce i diritti di accesso, modifica, creazione o eliminazione delle risorse per gruppo.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`groupHandle`*` | `xsd:string` | handle del gruppo. |
| ` *`groupName`*` | `xsd:string` | Nome del gruppo. |
| ` *`permissionsType`*` | `xsd:string` | Scelta del tipo di autorizzazione. |
| ` *`isAllowed`*` | `xsd:boolean` | Determina se l&#39;autorizzazione è consentita. |
| ` *`isOverride`*` | `xsd:boolean` | Determina se l&#39;autorizzazione sostituisce un&#39;altra. |

