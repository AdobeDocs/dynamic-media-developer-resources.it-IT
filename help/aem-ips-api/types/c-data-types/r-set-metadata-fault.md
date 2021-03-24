---
description: Dettagli di avviso o di errore per un aggiornamento dell'uso in un'operazione batchSetAssetMetadata.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic, SDK/API, Metadati
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 6%

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

