---
description: Descrive i metodi operativi nuovi e modificati per la versione 4.5 dell'API IPS.
solution: Experience Manager
title: Operazioni - Nuove e modificate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
TQID: 'https://experienceleague.adobe.com/n4U8LW8otIaBBDalW1wRJFaweTAw3-0Sh0ckgIEADAI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 0%

---

# Operazioni: nuove e modificate{#operations-new-and-modified}

Descrive i metodi operativi nuovi e modificati per la versione 4.5 dell&#39;API IPS.

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

* `Asset` include `animatedGifInfo`, `swcInfo`, `cssInfo` e `javascriptInfo` parametri.
* `createMetadataField` include un parametro `isHidden` facoltativo.
* `saveMetadataField` include un parametro `isHidden` facoltativo.
* `searchAssets`
* Il parametro `renameFiles` è stato dichiarato obsoleto per le versioni precedenti e rimosso dall&#39;operazione `renameAsset`. Il percorso del file virtuale viene modificato in modo da corrispondere al nuovo nome della risorsa (mantenendo l’estensione del file), mentre i percorsi dei file fisici non vengono interessati. I client API devono rimuovere i riferimenti a questo parametro durante l’aggiornamento alla nuova versione API.
