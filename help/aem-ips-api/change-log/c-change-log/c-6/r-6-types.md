---
description: Descrive i tipi nuovi e modificati per l’API IPS versione 6.
solution: Experience Manager
title: Tipi di dati nuovi e modificati
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# Tipi di dati: Nuovo e modificato{#data-types-new-and-modified}

Descrive i tipi nuovi e modificati per l’API IPS versione 6.

Sintassi

## Nuovi tipi {#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate`
* `AssetContextStateUpdateArray`
* `AssetPublishContexts`
* `AssetPublishContextsArray`
* `CompanyMember`
* `CompanyMemberArray`
* `CompanyMembershipUpdate`
* `CompanyMembershipUpdateArray`
* `ContextStateUpdate`
* `ContextStateUpdateArray`
* `Export Job`
* `PermissionsSet`
* `PermissionsSetArray`
* `PublishContext`
* `PublishContextArray`

## Tipi modificati {#section-56b834b1a3b843279d8715b4a4f3890b}

**Aggiunto**

* È stato aggiunto `numUrls` a `UploadUrlsJob`.

* Aggiunto `fileName` a `Asset.`

* È stato aggiunto `isHidden` a `MetadataField`.

* È stato aggiunto `taskState` a `TaskProgress`.

* Sono stati aggiunti `exportJob` a `ActiveJob` e `ScheduledJob`.

* Sono stati aggiunti `optmizedPath` e `optimizedFile` a `PsdInfo`.

* È stato aggiunto `contextHandle` a:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Sono stati aggiunti i seguenti parametri a `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Modificato**

* In `User`, è stato modificato `role` in `defaultRole`.

* In `Folder`, è stato modificato `permissions` in `permissionsSetHandle`.

* In `AssetSummary`, `type` e `name` sono ora facoltativi.

