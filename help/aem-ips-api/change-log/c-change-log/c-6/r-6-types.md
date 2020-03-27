---
description: Descrive i tipi nuovi e modificati per l'API IPS versione 6.
seo-description: Descrive i tipi nuovi e modificati per l'API IPS versione 6.
seo-title: Tipi di dati nuovi e modificati
solution: Experience Manager
title: Tipi di dati nuovi e modificati
topic: Scene7 Image Production System API
uuid: ef7c43ee-467f-46b9-bd82-05e8359bd829
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

* Aggiunto `optmizedPath` e `optimizedFile` a `PsdInfo`.

* Aggiunto `contextHandle` a:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Sono stati aggiunti i seguenti parametri a `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Modificato**

* In `User`, cambiato `role` in `defaultRole`.

* In `Folder`, cambiato `permissions` in `permissionsSetHandle`.

* In `AssetSummary`, `type` e ora `name` sono opzionali.

