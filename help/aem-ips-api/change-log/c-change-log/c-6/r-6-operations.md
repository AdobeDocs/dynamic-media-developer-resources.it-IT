---
description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 6.
solution: Experience Manager
title: Operazioni nuove e modificate
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
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

