---
title: AssetMetadataFields
description: Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 6%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

Restituisce le definizioni dei campi di metadati per i tipi di risorse specificati.

Sintassi

## Parametri {#section-5ad771540c5f40c187b35e34aac19305}

| Nome | Tipo | Descrizione |
|---|---|---|
| assetType | `xsd:string` | Tipo di risorsa associato alle definizioni dei campi (consulta &quot;Tipi di risorsa&quot; per i valori). |
| fieldArray | `types:MetadataFieldArray` | Array di definizioni dei campi di metadati associate al tipo di risorsa specificato in `assetType`. |
