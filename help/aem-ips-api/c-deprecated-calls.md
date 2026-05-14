---
title: Chiamate obsolete
description: Chiamate API di Image Production System e i relativi parametri associati non più utilizzati o supportati in [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
autotag-review: '2026-05-13T21:03:57.183Z'
TQID: 'https://experienceleague.adobe.com/JLoyXksHQ-LAXXxfY71Dv-FOE0trpt-RzcKcV-Pv96I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 0%

---

# Chiamate obsolete{#deprecated-calls}

Chiamate API del sistema di produzione delle immagini e i relativi parametri associati non più utilizzati.

## Chiamate obsolete {#topic-654c0466e6434fe4a95953322255b08c}

Chiamate API del sistema di produzione immagini e i relativi parametri associati non più utilizzati in [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS` - Obsoleto da [Tipi di dati](/help/aem-ips-api/types/c-data-types/c-data-types.md). Questo parametro escludeva il video principale dal set di video adattivi. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Obsoleto da [Operazioni](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Questo parametro consente di aggiungere un evento Media Portal a IPS.
* `getMediaPortalEvent` - Obsoleto da [Operazioni](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Questo parametro consente di ottenere eventi Media Portal corrispondenti ai criteri specificati.
* `getCdnCacheInvalidationStatus` - Obsoleto da [Operazioni](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Questo parametro è ora obsoleto perché il parametro `cdnCacheInvalidation` invalida la cache quasi immediatamente (~5 secondi). Di conseguenza, non è più necessario eseguire il polling per lo stato di invalidazione.
