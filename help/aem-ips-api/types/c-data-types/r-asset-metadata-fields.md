---
description: Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.
solution: Experience Manager
title: CampiMetadatiRisorsa
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---


# AssetMetadataFields{#assetmetadatafields}

Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.

Sintassi

## Parametri {#section-5ad771540c5f40c187b35e34aac19305}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Tipo di risorsa associato alle definizioni dei campi (vedere &quot;Tipi di risorse&quot; per i valori). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Array di definizioni di campi di metadati associate al tipo di risorsa specificato in `assetType`. |

