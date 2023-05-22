---
title: AssetOperationFault
description: Contiene informazioni sulle condizioni di avvertenza o di errore generate durante un'operazione di risorsa batch. I campi del codice e del motivo corrispondono ai campi del messaggio di errore che sarebbero stati generati per l'operazione non batch equivalente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 3%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

Contiene informazioni sulle condizioni di avvertenza o di errore generate durante un&#39;operazione di risorsa batch. I campi del codice e del motivo corrispondono ai campi del messaggio di errore che sarebbero stati generati per l&#39;operazione non batch equivalente.

Sintassi

## Parametri {#section-c906f052f43e4785ba46d92b514b0923}

| Nome | Tipo | Descrizione |
|---|---|---|
| assetHandle | `xsd:string` | Handle risorsa per l’operazione non riuscita. |
| codice | `xsd:int` | Codice di errore dell&#39;operazione. |
| motivo | `xsd:string` | Descrizione o motivo dell&#39;errore. |
