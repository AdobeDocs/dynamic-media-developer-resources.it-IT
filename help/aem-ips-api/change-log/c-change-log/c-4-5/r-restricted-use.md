---
description: Le operazioni e i tipi di dati nuovi o modificati disponibili nel file WSDL beta non devono essere utilizzati al di fuori delle applicazioni sviluppate in Scene7.
seo-description: Le operazioni e i tipi di dati nuovi o modificati disponibili nel file WSDL beta non devono essere utilizzati al di fuori delle applicazioni sviluppate in Scene7.
seo-title: Uso limitato
solution: Experience Manager
title: Uso limitato
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Uso limitato{#restricted-use}

Le operazioni e i tipi di dati nuovi o modificati disponibili nel file WSDL beta non devono essere utilizzati al di fuori delle applicazioni sviluppate in Scene7.

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

* Modificato `ActiveJob` per includere un `createVideoSitemapJob` tipo

* Modificato `ScheduledJob` per includere un `createVideoSitemapJob` tipo

* Modificato `ImageServingPublishJob` per includere un `contextHandle`

* Modificato `ImageRenderingPublishJob` per includere un `contextHandle`

* Modificato `MetadataField` per includere un `initialTagField`

* Modificato `MetadataCondition` in includi e `caseSensitive` parametro opzionale

* Modificato `PropertySet` per includere un facoltativo `PermissionArray` come `permissions`

* Modificato `UploadDirectoryJob` per includere parametri facoltativi `xmpKeywords`, `xmpTemplateId` e `xmpTemplateOverride`

* Modificato `VideoPublishJob` per includere un `contextHandle`

**Operazioni modificate**

* Modificato `createAssetSet` per includere un `thumbAssetHandle`

* Modificato `createImageSet` per includere un `thumbAssetHandle`

* Modificato `createMetadataField` per includere un `initialTagValue` parametro opzionale

* Modificato `createPropertySet` per includere un facoltativo `PermissionUpdateArray` come `permissionArray`

* Modificato `getImageServingPublishSettings` per includere un `contextHandle` parametro opzionale

* Modificato `getImageRenderingPublishSettings` per includere un `contextHandle` parametro opzionale

* Modificato `searchAssetsByFullText` per includere una serie di parametri opzionali:

   * `SearchFilter` come `filters` parametro

   * `sortBy`
   * `sortDirection`

* Modificato `searchAssetsByMetadata` per includere una serie di parametri opzionali:

   * `SearchFilter` come `filters` parametro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sequenza di sette parametri

* Modificato `setAssetPublishState` per includere un facoltativo `HandleArray` come `contextHandleArray`

* Modificato `setImageServingPublishSettings` per includere un `contextHandle` parametro opzionale

* Modificato `setImageRenderingPublishSettings` per includere un `contextHandle`parametro opzionale

* È stato modificato `submitJob` per includere un tipo di `createVideoSitemap` processo facoltativo

