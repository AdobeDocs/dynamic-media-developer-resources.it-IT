---
description: Descrive i metodi operativi nuovi e modificati per l’API IPS versione 4.5.
solution: Experience Manager
title: Operazioni nuove e modificate
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Operazioni: Nuovo e modificato{#operations-new-and-modified}

Descrive i metodi operativi nuovi e modificati per l’API IPS versione 4.5.

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

* `Asset` include  `animatedGifInfo`,  `swcInfo`,  `cssInfo` e  `javascriptInfo` parametri.

* `createMetadataField` include un  `isHidden` parametro opzionale.

* `saveMetadataField` include un  `isHidden` parametro opzionale.

* `searchAssets`
* 
* Il parametro `renameFiles` è stato dichiarato obsoleto per le versioni precedenti e rimosso dall&#39;operazione `renameAsset`. Il percorso del file virtuale viene modificato in modo che corrisponda al nuovo nome della risorsa (mantenendo l’estensione del file), mentre i percorsi dei file fisici non vengono interessati. I client API devono rimuovere i riferimenti a questo parametro quando si aggiorna alla nuova versione API.
