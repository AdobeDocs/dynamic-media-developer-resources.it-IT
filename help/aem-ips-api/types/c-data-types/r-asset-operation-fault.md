---
description: Contiene informazioni sulle condizioni di avviso o di errore generate durante un'operazione batch di risorse. I campi codice e motivo corrispondono ai campi messaggio di errore che sarebbero stati generati per l'operazione non batch equivalente.
seo-description: Contiene informazioni sulle condizioni di avviso o di errore generate durante un'operazione batch di risorse. I campi codice e motivo corrispondono ai campi messaggio di errore che sarebbero stati generati per l'operazione non batch equivalente.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Scene7 Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetOperationFault{#assetoperationfault}

Contiene informazioni sulle condizioni di avviso o di errore generate durante un&#39;operazione batch di risorse. I campi codice e motivo corrispondono ai campi messaggio di errore che sarebbero stati generati per l&#39;operazione non batch equivalente.

Sintassi

## Parametri {#section-c906f052f43e4785ba46d92b514b0923}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Handle risorsa per l&#39;operazione non riuscita. |
| ` *`code`*` | `xsd:int` | Codice di errore operativo. |
| ` *`reason`*` | `xsd:string` | Descrizione dell&#39;errore o motivo. |

