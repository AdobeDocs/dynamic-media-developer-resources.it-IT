---
description: Dettagli di avviso o di errore relativi a un aggiornamento dell’uso in un’operazione batchSetAssetMetadata.
seo-description: Dettagli di avviso o di errore relativi a un aggiornamento dell’uso in un’operazione batchSetAssetMetadata.
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Dynamic Media Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 5%

---


# SetMetadataFault{#setmetadatafault}

Dettagli di avviso o di errore relativi a un aggiornamento dell’uso in un’operazione batchSetAssetMetadata.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Risorsa i cui metadati non sono stati impostati correttamente. |
| `*`fieldHandle`*` | `xsd:string` | handle del campo di metadati il cui valore non è stato impostato correttamente. |
| `*`code`*` | `xsd:int` | Codice di errore. |
| `*`reason`*` | `xsd:string` | Descrizione errore (testo normale). |

