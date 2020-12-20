---
description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 4.5.
seo-description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 4.5.
seo-title: Operazioni nuove e modificate
solution: Experience Manager
title: Operazioni nuove e modificate
topic: Scene7 Image Production System API
uuid: c4002670-c830-474e-bb84-343f76b6fb80
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Operazioni: Nuovo e modificato{#operations-new-and-modified}

Descrive i metodi operativi nuovi e modificati per l&#39;API IPS versione 4.5.

Sintassi

## Nuove operazioni {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## Operazioni modificate {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` include  `animatedGifInfo`,  `swcInfo`,  `cssInfo`e  `javascriptInfo` parametri.

* `createMetadataField` include un  `isHidden` parametro facoltativo.

* `saveMetadataField` include un  `isHidden` parametro facoltativo.

* `searchAssets`
* 
* Il parametro `renameFiles` è stato dichiarato obsoleto per le versioni precedenti e rimosso dall&#39;operazione `renameAsset`. Il percorso del file virtuale viene modificato per corrispondere al nuovo nome della risorsa (mantenendo l’estensione del file), mentre i percorsi dei file fisici non vengono modificati. I client API devono rimuovere i riferimenti a questo parametro quando si aggiorna alla nuova versione dell&#39;API.

