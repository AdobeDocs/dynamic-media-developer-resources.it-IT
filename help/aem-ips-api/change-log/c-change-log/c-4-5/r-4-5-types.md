---
description: Descrive i tipi di dati nuovi e modificati per l’API IPS versione 4.5.
solution: Experience Manager
title: Tipi di dati nuovi e modificati
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# Tipi di dati: Nuovo e modificato{#data-types-new-and-modified}

Descrive i tipi di dati nuovi e modificati per l’API IPS versione 4.5.

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

* La risorsa include un nuovo campo `fileName` che restituisce il nome del file virtuale.
* `AssetSummary` restituisce un  `type` e un  `name` campo

* `MetadataField` include  `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` richiede un  `urlArray` e aggiunge un  `numUrls` conteggio facoltativo

