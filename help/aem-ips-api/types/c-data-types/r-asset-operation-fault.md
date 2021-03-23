---
description: Contiene informazioni sulle condizioni di avviso o di errore generate durante un’operazione batch di risorse. I campi codice e motivo corrispondono ai campi del messaggio di errore che sarebbero stati generati per l’operazione non batch equivalente.
seo-description: Contiene informazioni sulle condizioni di avviso o di errore generate durante un’operazione batch di risorse. I campi codice e motivo corrispondono ai campi del messaggio di errore che sarebbero stati generati per l’operazione non batch equivalente.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

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

