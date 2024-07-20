---
description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 6.
solution: Experience Manager
title: Operazioni nuove e modificate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
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

* Aggiunti `isHidden` e `initialTagValue` a:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Aggiunta di `thumbAssetHandle` a:

   * `createImageSet`
   * `createAssetSet`

  Aggiunta di `companyHandle` a:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

  Aggiunta di `contextHandle` a:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`

* IncludeInactive aggiunto a:

   * `getUsers`.
   * `getUserChars`.

* Aggiunta di `permissionArray` a `createPropertySet` completata.

* Aggiunta di `exportJob` a `submitJob` completata.

**Modificato**

* In `addUser` e `setUser`, è stato modificato `role` in `defaultRole`.

* In `getCompanyMembers`, è stato modificato `userArray` in `memberArray`.

* In `getCompanyMembership`, è stato modificato `companyArray` in `membershipArray`.

* In `addUser`, `setCompanyMembership` e `addCompanyMembership`, è stato modificato `membershipArray` in `companyHandleArray`.

* In `getCompanyMembership`, è stato modificato `companyArray` in `membershipArray`.

* In `getUserChars`, `includeInvalid` è ora facoltativo.

**Rimosso**

* Rimosso `renameFiles` da `renameAsset`.

* Rimosso `getXMPPanelViewDefinition`.
* Rimossi `searchAssetsByFulltext` e `searchAssetsBySimilarity`.
