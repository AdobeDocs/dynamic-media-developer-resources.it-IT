---
description: Informazioni sul registro di lavoro.
solution: Experience Manager
title: DettagliRegistroLavoro
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 6%

---

# DettagliRegistroLavoro{#joblogdetail}

Informazioni sul registro di lavoro.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| logMessage | `xsd:string` | Messaggi nel registro dei processi. |
| logType | `xsd:string` | Tipo di file registro processi. |
| assetName | `xsd:string` | Nome della risorsa nel registro processi (facoltativo). |
| assetType | `xsd:string` | Scelta del tipo di risorsa. |
| assetHandle | `xsd:string` | Handle di risorse a cui si fa riferimento nel registro processi. |
| auxArray | `types:JobLogDetailAuxArray` | Fornisce ulteriori informazioni dettagliate sul registro di lavoro oltre ai cinque tipi di log di processo descritti in precedenza. |
