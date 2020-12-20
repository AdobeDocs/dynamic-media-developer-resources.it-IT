---
description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 6.
seo-description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 6.
seo-title: Operazioni nuove e modificate
solution: Experience Manager
title: Operazioni nuove e modificate
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---


# Operazioni: Nuovo e modificato{#operations-new-and-modified}

Descrive i metodi operativi nuovi e modificati per l&#39;API IPS versione 6.

Sintassi

## Nuove operazioni {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## Operazioni modificate {#section-f4e8755527444266ae806e3f4c851ae6}

**Aggiunto**

* Aggiunti `isHidden` e `initialTagValue` a:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Aggiunto `thumbAssetHandle` a:

   * `createImageSet`
   * `createAssetSet`

   Aggiunto `companyHandle` a:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   Aggiunto `contextHandle` a:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* È stato aggiunto includeInactive a:

   * `getUsers`.
   * `getUserChars`.

* Aggiunto `permissionArray` a `createPropertySet`.

* Aggiunto `exportJob` a `submitJob`.

**Modificato**

* In `addUser` e `setUser`, è stato modificato `role` in `defaultRole`.

* In `getCompanyMembers`, è stato modificato `userArray` in `memberArray`.

* In `getCompanyMembership`, è stato modificato `companyArray` in `membershipArray`.

* In `addUser`, `setCompanyMembership` e `addCompanyMembership`, `membershipArray` è stato modificato in `companyHandleArray`.

* In `getCompanyMembership`, è stato modificato `companyArray` in `membershipArray`.

* In `getUserChars`, `includeInvalid` è ora opzionale.

**Rimosso**

* Rimosso `renameFiles` da `renameAsset`.

* Rimosso `getXMPPanelViewDefinition`.
* Rimosso `searchAssetsByFulltext` e `searchAssetsBySimilarity`.

