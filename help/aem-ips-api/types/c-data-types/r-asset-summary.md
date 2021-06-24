---
description: Risultati della ricerca di metadati contenenti informazioni riepilogate su una risorsa.
solution: Experience Manager
title: AssetSummary
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Developer,Administrator
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 6%

---

# AssetSummary{#assetsummary}

Risultati della ricerca di metadati contenenti informazioni riepilogate su una risorsa.

Sintassi

## Parametri {#section-ebc75cc024d94c439260d2e71873cc74}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Gestione risorse. |
| `*`type`*` | `xsd:string` | Tipo di risorsa. La costante &quot;Tipi di risorse&quot; definisce i possibili valori. Facoltativo. |
| `*`name`*` | `xsd:string` | Nome risorsa. Facoltativo. |
| `*`cartella`*` | `xsd:string` | La cartella contenente la risorsa. |
| `*`nomefile`*` | `xsd:string` | Nome file della risorsa. |
| `*`creato`*` | `xsd:dateTime` | Data creazione risorsa. |
| `*`createUser`*` | `xsd:string` | Utente che ha creato la risorsa. |
| `*`lastModified`*` | `xsd:dateTime` | Data dell’ultimo aggiornamento della risorsa. |
| `*`lastModifyUser`*` | `xsd:string` | Ultimo utente che ha modificato la risorsa. |
| `*`metadataArray`*` | `types:MetadataArray` | Array di valori di metadati associati alla risorsa. |
| `*`punteggio`*` | `xsd:double` | Definisce la precisione in caso di ricerca per similarità (0 = nessuna corrispondenza, 1 = corrispondenza esatta). |
| `*`scoreDetail`*` | `xsd:string` | Contiene informazioni dettagliate su aree simili a seguito di una ricerca per similarità. |
