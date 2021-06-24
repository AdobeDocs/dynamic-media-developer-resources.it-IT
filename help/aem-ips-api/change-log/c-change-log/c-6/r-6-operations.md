---
description: Descrive i metodi operativi nuovi e modificati per l’API IPS versione 6.
solution: Experience Manager
title: Operazioni nuove e modificate
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# Operazioni: Nuovo e modificato{#operations-new-and-modified}

Descrive i metodi operativi nuovi e modificati per l’API IPS versione 6.

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

* Sono stati aggiunti `isHidden` e `initialTagValue` a:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* È stato aggiunto `thumbAssetHandle` a:

   * `createImageSet`
   * `createAssetSet`

   È stato aggiunto `companyHandle` a:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   È stato aggiunto `contextHandle` a:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* È stato aggiunto includeInactive a:

   * `getUsers`.
   * `getUserChars`.

* È stato aggiunto `permissionArray` a `createPropertySet`.

* È stato aggiunto `exportJob` a `submitJob`.

**Modificato**

* In `addUser` e `setUser`, è stato modificato `role` in `defaultRole`.

* In `getCompanyMembers`, è stato modificato `userArray` in `memberArray`.

* In `getCompanyMembership`, è stato modificato `companyArray` in `membershipArray`.

* In `addUser`, `setCompanyMembership` e `addCompanyMembership`, `membershipArray` è stato modificato in `companyHandleArray`.

* In `getCompanyMembership`, è stato modificato `companyArray` in `membershipArray`.

* In `getUserChars`, `includeInvalid` è ora facoltativo.

**Rimosso**

* Rimosso `renameFiles` da `renameAsset`.

* Rimosso `getXMPPanelViewDefinition`.
* Rimossi `searchAssetsByFulltext` e `searchAssetsBySimilarity`.
