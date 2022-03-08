---
description: Dettagli di avviso o di errore per un aggiornamento dell'uso in un'operazione batchSetAssetMetadata.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# SetMetadataFault{#setmetadatafault}

Dettagli di avviso o di errore per un aggiornamento dell&#39;uso in un&#39;operazione batchSetAssetMetadata.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| assetHandle | `xsd:string` | Risorsa i cui metadati non sono stati impostati correttamente. |
| fieldHandle | `xsd:string` | L&#39;handle del campo metadati il cui valore è stato impostato in modo non corretto. |
| codice | `xsd:int` | Codice di errore. |
| motivo | `xsd:string` | Descrizione errore (testo normale). |
