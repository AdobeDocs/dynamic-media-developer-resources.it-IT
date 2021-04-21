---
description: Gestisce i diritti di accesso, modifica, creazione o eliminazione delle risorse per gruppo.
solution: Experience Manager
title: Autorizzazione
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 6%

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

