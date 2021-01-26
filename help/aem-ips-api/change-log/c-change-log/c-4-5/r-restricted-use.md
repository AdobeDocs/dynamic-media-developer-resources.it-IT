---
description: Le operazioni e i tipi di dati nuovi o modificati disponibili nel file WSDL beta non devono essere utilizzati al di fuori delle applicazioni sviluppate da Dynamic Media.
solution: Experience Manager
title: Uso limitato
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---


# Uso limitato{#restricted-use}

Le operazioni e i tipi di dati nuovi o modificati disponibili nel file WSDL beta non devono essere utilizzati al di fuori delle applicazioni sviluppate da Dynamic Media.

Tali operazioni e tipi sono soggetti a disabilitazione, modifica o rimozione dagli aggiornamenti di sistema successivi.

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
* batchGetAssetPublishContext
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContext
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

* Modificato `ActiveJob` per includere un tipo `createVideoSitemapJob`

* Modificato `ScheduledJob` per includere un tipo `createVideoSitemapJob`

* Modificato `ImageServingPublishJob` per includere un `contextHandle` facoltativo

* Modificato `ImageRenderingPublishJob` per includere un `contextHandle` facoltativo

* Modificato `MetadataField` per includere un `initialTagField` facoltativo

* Modificato `MetadataCondition` per includere e il parametro opzionale `caseSensitive`

* Modificato `PropertySet` per includere un `PermissionArray` facoltativo come `permissions`

* Modificato `UploadDirectoryJob` per includere i parametri opzionali `xmpKeywords`, `xmpTemplateId` e `xmpTemplateOverride`

* Modificato `VideoPublishJob` per includere un `contextHandle` facoltativo

**Operazioni modificate**

* Modificato `createAssetSet` per includere un `thumbAssetHandle` facoltativo

* Modificato `createImageSet` per includere un `thumbAssetHandle` facoltativo

* Modificato `createMetadataField` per includere un parametro opzionale `initialTagValue`

* Modificato `createPropertySet` per includere un `PermissionUpdateArray` facoltativo come `permissionArray`

* Modificato `getImageServingPublishSettings` per includere un parametro opzionale `contextHandle`

* Modificato `getImageRenderingPublishSettings` per includere un parametro opzionale `contextHandle`

* Modificato `searchAssetsByFullText` per includere una serie di parametri opzionali:

   * `SearchFilter` as,  `filters` parametro

   * `sortBy`
   * `sortDirection`

* Modificato `searchAssetsByMetadata` per includere una serie di parametri opzionali:

   * `SearchFilter` as,  `filters` parametro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sequenza di sette parametri

* Modificato `setAssetPublishState` per includere un `HandleArray` facoltativo come `contextHandleArray`

* Modificato `setImageServingPublishSettings` per includere un parametro opzionale `contextHandle`

* Modificato `setImageRenderingPublishSettings` per includere un parametro opzionale `contextHandle`

* Modificato `submitJob` per includere un tipo di processo `createVideoSitemap` facoltativo

