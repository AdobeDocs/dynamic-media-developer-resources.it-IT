---
description: Gestisce i diritti di accesso, modifica, creazione o eliminazione delle risorse per gruppo.
solution: Experience Manager
title: Autorizzazione
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 7%

---

# [!DNL Permission]{#permission}

Gestisce i diritti di accesso, modifica, creazione o eliminazione delle risorse per gruppo.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| groupHandle | `xsd:string` | Maniglia di gruppo. |
| groupName | `xsd:string` | Nome del gruppo. |
| permissionType | `xsd:string` | Scelta del tipo di autorizzazione. |
| isAllowed | `xsd:boolean` | Determina se l&#39;autorizzazione è consentita. |
| isOverride | `xsd:boolean` | Determina se l&#39;autorizzazione sostituisce un&#39;altra. |
