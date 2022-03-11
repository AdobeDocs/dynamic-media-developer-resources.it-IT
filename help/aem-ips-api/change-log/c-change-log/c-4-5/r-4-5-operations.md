---
description: Descrive i metodi operativi nuovi e modificati per l’API IPS versione 4.5.
solution: Experience Manager
title: Operazioni - Nuove e modificate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '98'
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

* `Asset` include `animatedGifInfo`, `swcInfo`, `cssInfo`e `javascriptInfo` Parametri.
* `createMetadataField` include un `isHidden` parametro .
* `saveMetadataField` include un `isHidden` parametro .
* `searchAssets`
* La `renameFiles` è stato dichiarato obsoleto per le versioni precedenti e rimosso dalla `renameAsset` funzionamento. Il percorso del file virtuale viene modificato in modo che corrisponda al nuovo nome della risorsa (mantenendo l’estensione del file), mentre i percorsi dei file fisici non vengono interessati. I client API devono rimuovere i riferimenti a questo parametro quando si aggiorna alla nuova versione API.
