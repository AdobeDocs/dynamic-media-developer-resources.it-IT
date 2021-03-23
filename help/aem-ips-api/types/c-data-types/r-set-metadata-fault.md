---
description: Dettagli di avviso o di errore per un aggiornamento dell'uso in un'operazione batchSetAssetMetadata.
seo-description: Dettagli di avviso o di errore per un aggiornamento dell'uso in un'operazione batchSetAssetMetadata.
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
feature: Dynamic Media Classic, SDK/API, Metadati
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# SetMetadataFault{#setmetadatafault}

Dettagli di avviso o di errore per un aggiornamento dell&#39;uso in un&#39;operazione batchSetAssetMetadata.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Risorsa i cui metadati non sono stati impostati correttamente. |
| `*`fieldHandle`*` | `xsd:string` | L&#39;handle del campo metadati il cui valore è stato impostato in modo non corretto. |
| `*`codice`*` | `xsd:int` | Codice di errore. |
| `*`motivo`*` | `xsd:string` | Descrizione errore (testo normale). |

