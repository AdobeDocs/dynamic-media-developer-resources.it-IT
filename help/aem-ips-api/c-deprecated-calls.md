---
title: Chiamate obsolete
description: Chiamate API di Image Production System e i relativi parametri associati che non sono più utilizzati o supportati in Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 72f9cd1b1de82cbeeb8d41fb0f1cf0b51744a8a3
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# Chiamate obsolete{#deprecated-calls}

Chiamate API di Image Production System e i relativi parametri associati che non vengono più utilizzati.

## Chiamate obsolete {#topic-654c0466e6434fe4a95953322255b08c}

Chiamate API di Image Production System e i relativi parametri associati che non vengono più utilizzati in Dynamic Media.

* `ExcludeMasterVideoFromAVS` - Obsoleto di [Tipi di dati](/help/aem-ips-api/types/c-data-types/c-data-types.md). Questo parametro ha escluso il video principale dal set di video adattivi. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Obsoleto di [Operazioni](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Questo parametro consente di aggiungere un evento Media Portal all’IPS.
* `getMediaPortalEvent` - Obsoleto di [Operazioni](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Questo parametro consente di ottenere eventi del portale multimediale che corrispondono a criteri specifici.
* `getCdnCacheInvalidationStatus` - Obsoleto di [Operazioni](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Questo parametro è diventato obsoleto perché la `cdnCacheInvalidation` Il parametro invalida la cache quasi immediatamente (~5 secondi). Di conseguenza, non è più necessario eseguire il polling per lo stato di invalidazione.
