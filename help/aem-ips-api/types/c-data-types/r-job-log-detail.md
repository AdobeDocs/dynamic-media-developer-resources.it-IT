---
description: Informazioni sul registro dei processi.
seo-description: Informazioni sul registro dei processi.
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
topic: Scene7 Image Production System API
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JobLogDetail{#joblogdetail}

Informazioni sul registro dei processi.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`logMessage`*` | `xsd:string` | Messaggi nel registro processi. |
| ` *`logType`*` | `xsd:string` | Tipo di file registro processo. |
| ` *`assetName`*` | `xsd:string` | Nome della risorsa nel registro dei processi (facoltativo). |
| ` *`assetType`*` | `xsd:string` | Scelta del tipo di risorsa. |
| ` *`assetHandle`*` | `xsd:string` | Handle risorsa a cui si fa riferimento nel registro processi. |
| ` *`auxArray`*` | `types:JobLogDetailAuxArray` | Fornisce ulteriori informazioni dettagliate sul registro dei processi oltre i cinque tipi di registro processi descritti in precedenza. |

