---
title: Chiamate obsolete
description: Chiamate API di Image Production System e i relativi parametri associati che non sono più utilizzati o supportati in Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Chiamate obsolete{#deprecated-calls}

Chiamate API di Image Production System e i relativi parametri associati che non vengono più utilizzati.

## Chiamate obsolete {#topic-654c0466e6434fe4a95953322255b08c}

Chiamate API di Image Production System e i relativi parametri associati che non vengono più utilizzati in Dynamic Media.

* `ExcludeMasterVideoFromAVS` - Obsoleto di [Tipi di dati](/help/aem-ips-api/types/c-data-types/c-data-types.md). Questo parametro ha escluso il video principale dal set di video adattivi.
   >[!IMPORTANT]
   >
   >Adobe cesserà il supporto per questo parametro il 1° settembre 2022. Vedi anche [ExcludeMasterVideoFromAVS](/help/aem-ips-api/types/c-data-types/r-exclude-master-video-from-avs.md).
* `addMediaPortalEvent` - Obsoleto di [Operazioni](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Questo parametro consente di aggiungere un evento Media Portal all’IPS.
* `getMediaPortalEvent` - Obsoleto di [Operazioni](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Questo parametro consente di ottenere eventi del portale multimediale che corrispondono a criteri specifici.
* `getCdnCacheInvalidationStatus` - Obsoleto di [Operazioni](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Questo parametro è diventato obsoleto perché la `cdnCacheInvalidation` Il parametro invalida la cache quasi immediatamente (~5 secondi). Di conseguenza, non è più necessario eseguire il polling per lo stato di invalidazione.
