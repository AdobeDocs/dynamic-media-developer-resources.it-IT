---
description: Descrive i tipi nuovi e modificati per l’API IPS versione 6.
solution: Experience Manager
title: Tipi di dati nuovi e modificati
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '74'
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
