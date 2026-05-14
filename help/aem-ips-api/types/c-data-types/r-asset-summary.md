---
title: Riepilogo risorse
description: Risultati della ricerca di metadati che contengono informazioni di riepilogo su una risorsa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
TQID: 'https://experienceleague.adobe.com/RHT8NJiS0pGKUcrYGBsSI1vewvRGUCZmsPYP6Pb0OBs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 4%

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
