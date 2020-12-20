---
description: Risultati della ricerca di metadati contenenti informazioni riepilogate su una risorsa.
seo-description: Risultati della ricerca di metadati contenenti informazioni riepilogate su una risorsa.
seo-title: AssetSummary
solution: Experience Manager
title: AssetSummary
topic: Scene7 Image Production System API
uuid: 0ac8f900-c16c-409d-b83c-3bdf0ad28fac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 6%

---


# AssetSummary{#assetsummary}

Risultati della ricerca di metadati contenenti informazioni riepilogate su una risorsa.

Sintassi

## Parametri {#section-ebc75cc024d94c439260d2e71873cc74}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Handle risorsa. |
| ` *`type`*` | `xsd:string` | Tipo di risorsa. La costante &quot;Asset Types&quot; definisce i valori possibili. Facoltativo. |
| ` *`name`*` | `xsd:string` | Nome risorsa. Facoltativo. |
| ` *`folder`*` | `xsd:string` | La cartella che contiene la risorsa. |
| ` *`nomefile`*` | `xsd:string` | Nome file della risorsa. |
| ` *`created`*` | `xsd:dateTime` | Data creazione risorsa. |
| ` *`createUser`*` | `xsd:string` | L’utente che ha creato la risorsa. |
| ` *`lastModified`*` | `xsd:dateTime` | Data dell’ultimo aggiornamento della risorsa. |
| ` *`lastModifyUser`*` | `xsd:string` | Ultimo utente che ha modificato la risorsa. |
| ` *`metadataArray`*` | `types:MetadataArray` | Array di valori di metadati associati alla risorsa. |
| ` *`score`*` | `xsd:double` | Definisce la precisione nel caso di una ricerca per similarità (0 = no match, 1 = exact match). |
| ` *`scoreDetail`*` | `xsd:string` | Contiene informazioni dettagliate su aree simili a seguito di una ricerca per similarità. |

