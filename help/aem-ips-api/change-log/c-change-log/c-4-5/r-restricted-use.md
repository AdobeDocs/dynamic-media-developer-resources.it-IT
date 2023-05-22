---
description: Le operazioni e i tipi di dati nuovi o modificati disponibili nel file WSDL beta non devono essere utilizzati al di fuori delle applicazioni sviluppate da Dynamic Media.
solution: Experience Manager
title: Uso limitato
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Uso limitato{#restricted-use}

Le operazioni e i tipi di dati nuovi o modificati disponibili nel file WSDL beta non devono essere utilizzati al di fuori delle applicazioni sviluppate da Dynamic Media.

Queste operazioni e tipi sono soggetti a disabilitazione, modifica o rimozione con successivi aggiornamenti di sistema.

**Nuovi tipi**

* AssetPublishContexts
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

* Modificato `ActiveJob` per includere un `createVideoSitemapJob` tipo

* Modificato `ScheduledJob` per includere un `createVideoSitemapJob` tipo

* Modificato `ImageServingPublishJob` per includere un `contextHandle`

* Modificato `ImageRenderingPublishJob` per includere un `contextHandle`

* Modificato `MetadataField` per includere un `initialTagField`

* Modificato `MetadataCondition` da includere e facoltativo `caseSensitive` parametro

* Modificato `PropertySet` per includere un `PermissionArray` as `permissions`

* Modificato `UploadDirectoryJob` per includere elementi opzionali `xmpKeywords`, `xmpTemplateId` e `xmpTemplateOverride` parametri

* Modificato `VideoPublishJob` per includere un `contextHandle`

**Operazioni modificate**

* Modificato `createAssetSet` per includere un `thumbAssetHandle`

* Modificato `createImageSet` per includere un `thumbAssetHandle`

* Modificato `createMetadataField` per includere un `initialTagValue` parametro

* Modificato `createPropertySet` per includere un `PermissionUpdateArray` as `permissionArray`

* Modificato `getImageServingPublishSettings` per includere un `contextHandle` parametro

* Modificato `getImageRenderingPublishSettings` per includere un `contextHandle` parametro

* Modificato `searchAssetsByFullText` per includere una serie di parametri facoltativi:

   * `SearchFilter` as `filters` parametro

   * `sortBy`
   * `sortDirection`

* Modificato `searchAssetsByMetadata` per includere una serie di parametri facoltativi:

   * `SearchFilter` as `filters` parametro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sequenza di sette parametri

* Modificato `setAssetPublishState` per includere un `HandleArray` as `contextHandleArray`

* Modificato `setImageServingPublishSettings` per includere un `contextHandle` parametro

* Modificato `setImageRenderingPublishSettings` per includere un `contextHandle`parametro

* Modificato `submitJob` per includere un `createVideoSitemap` tipo di processo
