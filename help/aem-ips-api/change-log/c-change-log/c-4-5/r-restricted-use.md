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

* `ActiveJob` è stato modificato per includere un tipo `createVideoSitemapJob`

* `ScheduledJob` è stato modificato per includere un tipo `createVideoSitemapJob`

* `ImageServingPublishJob` è stato modificato per includere un elemento `contextHandle` facoltativo

* `ImageRenderingPublishJob` è stato modificato per includere un elemento `contextHandle` facoltativo

* `MetadataField` è stato modificato per includere un elemento `initialTagField` facoltativo

* `MetadataCondition` è stato modificato per includere e includere il parametro facoltativo `caseSensitive`

* `PropertySet` è stato modificato per includere un `PermissionArray` facoltativo come `permissions`

* `UploadDirectoryJob` è stato modificato per includere i parametri facoltativi `xmpKeywords`, `xmpTemplateId` e `xmpTemplateOverride`

* `VideoPublishJob` è stato modificato per includere un elemento `contextHandle` facoltativo

**Operazioni modificate**

* `createAssetSet` è stato modificato per includere un elemento `thumbAssetHandle` facoltativo

* `createImageSet` è stato modificato per includere un elemento `thumbAssetHandle` facoltativo

* `createMetadataField` è stato modificato per includere un parametro `initialTagValue` facoltativo

* `createPropertySet` è stato modificato per includere un `PermissionUpdateArray` facoltativo come `permissionArray`

* `getImageServingPublishSettings` è stato modificato per includere un parametro `contextHandle` facoltativo

* `getImageRenderingPublishSettings` è stato modificato per includere un parametro `contextHandle` facoltativo

* `searchAssetsByFullText` è stato modificato per includere una serie di parametri facoltativi:

   * `SearchFilter` come parametro `filters`

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata` è stato modificato per includere una serie di parametri facoltativi:

   * `SearchFilter` come parametro `filters`

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sequenza di sette parametri

* `setAssetPublishState` è stato modificato per includere un `HandleArray` facoltativo come `contextHandleArray`

* `setImageServingPublishSettings` è stato modificato per includere un parametro `contextHandle` facoltativo

* `setImageRenderingPublishSettings` è stato modificato per includere un parametro `contextHandle` facoltativo

* `submitJob` è stato modificato per includere un tipo di processo `createVideoSitemap` facoltativo
