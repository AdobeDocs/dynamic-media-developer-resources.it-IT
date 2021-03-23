---
description: Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.
seo-description: Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.
seo-title: CampiMetadatiRisorsa
solution: Experience Manager
title: CampiMetadatiRisorsa
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
feature: Dynamic Media Classic, SDK/API, metadati, gestione delle risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 5%

---


# AssetMetadataFields{#assetmetadatafields}

Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.

Sintassi

## Parametri {#section-5ad771540c5f40c187b35e34aac19305}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Tipo di risorsa associato alle definizioni dei campi (vedere &quot;Tipi di risorse&quot; per i valori). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Array di definizioni di campi di metadati associate al tipo di risorsa specificato in `assetType`. |

