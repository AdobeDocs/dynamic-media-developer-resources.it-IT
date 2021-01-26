---
description: Descrive i tipi nuovi e modificati per l'API IPS versione 6.
solution: Experience Manager
title: Tipi di dati nuovi e modificati
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---


# Tipi di dati: Nuovo e modificato{#data-types-new-and-modified}

Descrive i tipi nuovi e modificati per l&#39;API IPS versione 6.

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

* Aggiunto `numUrls` a `UploadUrlsJob`.

* Aggiunto `fileName` a `Asset.`

* Aggiunto `isHidden` a `MetadataField`.

* Aggiunto `taskState` a `TaskProgress`.

* Aggiunto `exportJob` a `ActiveJob` e `ScheduledJob`.

* Sono stati aggiunti `optmizedPath` e `optimizedFile` a `PsdInfo`.

* Aggiunto `contextHandle` a:

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

