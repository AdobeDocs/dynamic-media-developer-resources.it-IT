---
description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 6.
solution: Experience Manager
title: Operazioni nuove e modificate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# Operazioni: nuove e modificate{#operations-new-and-modified}

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

* Aggiunto `isHidden` e `initialTagValue` a:

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



* IncludeInactive aggiunto a:

   * `getUsers`.
   * `getUserChars`.

* Aggiunto `permissionArray` a `createPropertySet`.

* Aggiunto `exportJob` a `submitJob`.

**Modificato**

* In entrata `addUser` e `setUser`, modificato `role` a `defaultRole`.

* In entrata `getCompanyMembers`, modificato `userArray` a `memberArray`.

* In entrata `getCompanyMembership`, modificato `companyArray` a `membershipArray`.

* In entrata `addUser`, `setCompanyMembership`, e `addCompanyMembership`, modificato `membershipArray` a `companyHandleArray`.

* In entrata `getCompanyMembership`, modificato `companyArray` a `membershipArray`.

* In entrata `getUserChars`, `includeInvalid` è ora facoltativo.

**Rimosso**

* Rimosso `renameFiles` da `renameAsset`.

* Rimosso `getXMPPanelViewDefinition`.
* Rimosso `searchAssetsByFulltext` e `searchAssetsBySimilarity`.
