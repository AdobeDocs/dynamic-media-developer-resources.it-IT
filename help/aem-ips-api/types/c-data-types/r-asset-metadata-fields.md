---
description: Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.
solution: Experience Manager
title: CampiMetadatiRisorsa
feature: Dynamic Media Classic, SDK/API, metadati, gestione delle risorse
role: Developer,Administrator
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 7%

---

# CampiMetadatiRisorsa{#assetmetadatafields}

Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.

Sintassi

## Parametri {#section-5ad771540c5f40c187b35e34aac19305}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Tipo di risorsa associato alle definizioni dei campi (vedere &quot;Tipi di risorse&quot; per i valori). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Array di definizioni di campi di metadati associate al tipo di risorsa specificato in `assetType`. |
