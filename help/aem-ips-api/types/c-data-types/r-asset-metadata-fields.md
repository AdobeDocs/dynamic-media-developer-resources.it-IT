---
description: Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.
seo-description: Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
topic: Scene7 Image Production System API
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetMetadataFields{#assetmetadatafields}

Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.

Sintassi

## Parametri {#section-5ad771540c5f40c187b35e34aac19305}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`assetType`*` | `xsd:string` | Tipo di risorsa associato alle definizioni dei campi (vedere &quot;Tipi di risorse&quot; per i valori). |
| ` *`fieldArray`*` | `types:MetadataFieldArray` | Array di definizioni dei campi di metadati associate al tipo di risorsa specificato in `assetType`. |

