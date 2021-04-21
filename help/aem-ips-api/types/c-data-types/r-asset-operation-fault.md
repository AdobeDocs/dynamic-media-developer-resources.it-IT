---
description: Contiene informazioni sulle condizioni di avviso o di errore generate durante un’operazione batch di risorse. I campi codice e motivo corrispondono ai campi del messaggio di errore che sarebbero stati generati per l’operazione non batch equivalente.
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---


# AssetOperationFault{#assetoperationfault}

Contiene informazioni sulle condizioni di avviso o di errore generate durante un’operazione batch di risorse. I campi codice e motivo corrispondono ai campi del messaggio di errore che sarebbero stati generati per l’operazione non batch equivalente.

Sintassi

## Parametri {#section-c906f052f43e4785ba46d92b514b0923}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Handle risorsa per l’operazione non riuscita. |
| `*`codice`*` | `xsd:int` | Codice di errore dell&#39;operazione. |
| `*`motivo`*` | `xsd:string` | Descrizione o motivo di errore. |

