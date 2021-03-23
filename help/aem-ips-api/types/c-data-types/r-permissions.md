---
description: Gestisce i diritti di accesso, modifica, creazione o eliminazione delle risorse per gruppo.
seo-description: Gestisce i diritti di accesso, modifica, creazione o eliminazione delle risorse per gruppo.
seo-title: Autorizzazione
solution: Experience Manager
title: Autorizzazione
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---


# Permesso{#permission}

Gestisce i diritti di accesso, modifica, creazione o eliminazione delle risorse per gruppo.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Maniglia di gruppo. |
| `*`groupName`*` | `xsd:string` | Nome del gruppo. |
| `*`permissionType`*` | `xsd:string` | Scelta del tipo di autorizzazione. |
| `*`isAllowed`*` | `xsd:boolean` | Determina se l&#39;autorizzazione è consentita. |
| `*`isOverride`*` | `xsd:boolean` | Determina se l&#39;autorizzazione sostituisce un&#39;altra. |

