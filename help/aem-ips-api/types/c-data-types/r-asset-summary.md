---
title: Riepilogo risorse
description: Risultati della ricerca di metadati che contengono informazioni di riepilogo su una risorsa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 5%

---

# [!DNL AssetSummary]{#assetsummary}

Risultati della ricerca di metadati che contengono informazioni di riepilogo su una risorsa.

Sintassi

## Parametri {#section-ebc75cc024d94c439260d2e71873cc74}

| Nome | Tipo | Descrizione |
|---|---|---|
| assetHandle | `xsd:string` | Handle risorsa. |
| tipo | `xsd:string` | Tipo di risorsa. La costante &quot;Tipi di risorsa&quot; definisce i valori possibili. Facoltativo. |
| nome | `xsd:string` | Nome risorsa. Facoltativo. |
| cartella | `xsd:string` | Cartella che contiene la risorsa. |
| nome file | `xsd:string` | Nome file della risorsa. |
| creato | `xsd:dateTime` | Data di creazione risorsa. |
| createUser | `xsd:string` | Utente che ha creato la risorsa. |
| lastModified | `xsd:dateTime` | Data dell’ultimo aggiornamento della risorsa. |
| lastModifyUser | `xsd:string` | L’ultimo utente che ha modificato la risorsa. |
| metadataArray | `types:MetadataArray` | Array di valori di metadati associati alla risorsa. |
| punteggio | `xsd:double` | Definisce la precisione in caso di ricerca per similarità (0 = nessuna corrispondenza, 1 = corrispondenza esatta). |
| scoreDetail | `xsd:string` | Contiene informazioni dettagliate su aree simili a seguito di una ricerca per similarità. |
