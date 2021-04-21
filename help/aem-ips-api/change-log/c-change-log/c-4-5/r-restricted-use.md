---
description: Le operazioni e i tipi di dati nuovi o modificati disponibili nella versione beta WSDL non devono essere utilizzati al di fuori delle applicazioni sviluppate da Dynamic Media.
solution: Experience Manager
title: Uso limitato
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Uso limitato{#restricted-use}

Le operazioni e i tipi di dati nuovi o modificati disponibili nella versione beta WSDL non devono essere utilizzati al di fuori delle applicazioni sviluppate da Dynamic Media.

Queste operazioni e questi tipi sono soggetti a disabilitazione, modifica o rimozione con gli aggiornamenti successivi del sistema.

**Nuovi tipi**

* AssetPublishContext
* AssetPublishContextsArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**Nuove operazioni**

* applyMetadataTemplate
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContexts
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBySimilarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**Tipi modificati**

* È stato modificato `ActiveJob` per includere un tipo `createVideoSitemapJob`

* È stato modificato `ScheduledJob` per includere un tipo `createVideoSitemapJob`

* È stato modificato `ImageServingPublishJob` in modo da includere un `contextHandle` facoltativo

* È stato modificato `ImageRenderingPublishJob` in modo da includere un `contextHandle` facoltativo

* È stato modificato `MetadataField` in modo da includere un `initialTagField` facoltativo

* È stato modificato `MetadataCondition` per includere e il parametro opzionale `caseSensitive`

* È stato modificato `PropertySet` in modo da includere un `PermissionArray` facoltativo come `permissions`

* Modificato `UploadDirectoryJob` per includere i parametri facoltativi `xmpKeywords`, `xmpTemplateId` e `xmpTemplateOverride`

* È stato modificato `VideoPublishJob` in modo da includere un `contextHandle` facoltativo

**Operazioni modificate**

* È stato modificato `createAssetSet` in modo da includere un `thumbAssetHandle` facoltativo

* È stato modificato `createImageSet` in modo da includere un `thumbAssetHandle` facoltativo

* È stato modificato `createMetadataField` per includere un parametro opzionale `initialTagValue`

* È stato modificato `createPropertySet` in modo da includere un `PermissionUpdateArray` facoltativo come `permissionArray`

* È stato modificato `getImageServingPublishSettings` per includere un parametro opzionale `contextHandle`

* È stato modificato `getImageRenderingPublishSettings` per includere un parametro opzionale `contextHandle`

* È stata modificata `searchAssetsByFullText` per includere una serie di parametri facoltativi:

   * `SearchFilter` come  `filters` parametro

   * `sortBy`
   * `sortDirection`

* È stata modificata `searchAssetsByMetadata` per includere una serie di parametri facoltativi:

   * `SearchFilter` come  `filters` parametro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sequenza di sette parametri

* È stato modificato `setAssetPublishState` in modo da includere un `HandleArray` facoltativo come `contextHandleArray`

* È stato modificato `setImageServingPublishSettings` per includere un parametro opzionale `contextHandle`

* È stato modificato `setImageRenderingPublishSettings` per includere un parametro opzionale `contextHandle`.

* È stato modificato `submitJob` per includere un tipo di processo `createVideoSitemap` facoltativo

