---
description: Informazioni sul registro di lavoro.
solution: Experience Manager
title: DettagliRegistroLavoro
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---


# JobLogDetail{#joblogdetail}

Informazioni sul registro di lavoro.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Messaggi nel registro dei processi. |
| `*`logType`*` | `xsd:string` | Tipo di file registro processi. |
| `*`assetName`*` | `xsd:string` | Nome della risorsa nel registro processi (facoltativo). |
| `*`assetType`*` | `xsd:string` | Scelta del tipo di risorsa. |
| `*`assetHandle`*` | `xsd:string` | Handle di risorse a cui si fa riferimento nel registro processi. |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | Fornisce ulteriori informazioni dettagliate sul registro di lavoro oltre ai cinque tipi di log di processo descritti in precedenza. |

