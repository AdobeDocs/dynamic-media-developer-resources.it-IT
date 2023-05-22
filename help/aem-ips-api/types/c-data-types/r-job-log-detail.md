---
description: Informazioni registro processo.
solution: Experience Manager
title: DettagliRegistroProcesso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 5%

---

# [!DNL JobLogDetail]{#joblogdetail}

Informazioni registro processo.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| logMessage | `xsd:string` | Messaggi nel registro del processo. |
| logType | `xsd:string` | Tipo di file registro processo. |
| assetName | `xsd:string` | Nome della risorsa nel registro del processo (facoltativo). |
| assetType | `xsd:string` | Scelta del tipo di risorsa. |
| assetHandle | `xsd:string` | Handle di risorsa a cui si fa riferimento nel registro del processo. |
| auxArray | `types:JobLogDetailAuxArray` | Fornisce informazioni dettagliate aggiuntive sul registro di processo oltre ai cinque tipi di registro di processo descritti in precedenza. |
