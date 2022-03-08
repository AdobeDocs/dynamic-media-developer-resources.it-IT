---
title: AssetOperationFault
description: Contiene informazioni sulle condizioni di avviso o di errore generate durante un’operazione batch di risorse. I campi codice e motivo corrispondono ai campi del messaggio di errore che sarebbero stati generati per l’operazione non batch equivalente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---

# AssetOperationFault{#assetoperationfault}

Contiene informazioni sulle condizioni di avviso o di errore generate durante un’operazione batch di risorse. I campi codice e motivo corrispondono ai campi del messaggio di errore che sarebbero stati generati per l’operazione non batch equivalente.

Sintassi

## Parametri {#section-c906f052f43e4785ba46d92b514b0923}

| Nome | Tipo | Descrizione |
|---|---|---|
| assetHandle | `xsd:string` | Handle risorsa per l’operazione non riuscita. |
| codice | `xsd:int` | Codice di errore dell&#39;operazione. |
| motivo | `xsd:string` | Descrizione o motivo di errore. |
