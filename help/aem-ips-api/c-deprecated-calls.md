---
title: Chiamate obsolete
description: Chiamate API Image Production System e relativi parametri associati non più utilizzati in Dynamic Media.
solution: Experience Manager
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Chiamate obsolete{#deprecated-calls}

Chiamate API Image Production System e relativi parametri associati non più utilizzati.

## Chiamate obsolete {#topic-654c0466e6434fe4a95953322255b08c}

Chiamate API Image Production System e relativi parametri associati non più utilizzati in Dynamic Media.

* `addMediaPortalEvent` - Obsoleto da Operazioni. Questa chiamata consente di aggiungere un evento Media Portal a IPS.
* `getMediaPortalEvent` - Obsoleto da Operazioni. Questa chiamata consente di ottenere eventi del portale multimediale che corrispondono a criteri specifici.
* `getCdnCacheInvalidationStatus` - Obsoleto da Operazioni. Questa API ora è obsoleta perché l&#39;API `cdnCacheInvalidation` invalida la cache quasi immediatamente (~5 secondi). Di conseguenza, il polling per lo stato di annullamento della validità non è più necessario.

