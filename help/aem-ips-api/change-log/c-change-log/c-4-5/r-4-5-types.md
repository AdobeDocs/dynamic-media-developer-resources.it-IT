---
description: Descrive i tipi di dati nuovi e modificati per la versione 4.5 dell'API IPS.
solution: Experience Manager
title: Tipi di dati nuovi e modificati
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# Tipi di dati: nuovi e modificati{#data-types-new-and-modified}

Descrive i tipi di dati nuovi e modificati per la versione 4.5 dell&#39;API IPS.

Sintassi

## Nuovi tipi {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## Tipi modificati {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* La risorsa include una nuova `fileName` che restituisce il nome del file virtuale.
* `AssetSummary` restituisce un `type` e `name` campo

* `MetadataField` include `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` richiede un `urlArray` e aggiunge un `numUrls` count
