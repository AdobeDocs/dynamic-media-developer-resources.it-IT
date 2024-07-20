---
description: Vengono descritti i tipi nuovi e modificati per l'API IPS versione 6.
solution: Experience Manager
title: Tipi di dati nuovi e modificati
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# Tipi di dati: nuovi e modificati{#data-types-new-and-modified}

Vengono descritti i tipi nuovi e modificati per l&#39;API IPS versione 6.

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

* Aggiunta di `numUrls` a `UploadUrlsJob` completata.

* Aggiunto `fileName` a `Asset.`

* Aggiunta di `isHidden` a `MetadataField` completata.

* Aggiunta di `taskState` a `TaskProgress` completata.

* Aggiunto `exportJob` a `ActiveJob` e `ScheduledJob`.

* Aggiunti `optmizedPath` e `optimizedFile` a `PsdInfo`.

* Aggiunta di `contextHandle` a:

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
