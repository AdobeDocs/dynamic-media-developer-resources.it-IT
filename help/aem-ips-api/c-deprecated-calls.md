---
title: Chiamate obsolete
description: Chiamate API di Image Production System e i relativi parametri associati che non vengono più utilizzati in Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Chiamate obsolete{#deprecated-calls}

Chiamate API di Image Production System e i relativi parametri associati che non vengono più utilizzati.

## Chiamate obsolete {#topic-654c0466e6434fe4a95953322255b08c}

Chiamate API di Image Production System e i relativi parametri associati che non vengono più utilizzati in Dynamic Media.

* `addMediaPortalEvent` - Operazioni obsolete. Questa chiamata ti consente di aggiungere un evento Media Portal all’IPS.
* `getMediaPortalEvent` - Operazioni obsolete. Questa chiamata ti consente di ottenere eventi del portale multimediale che corrispondono a criteri specifici.
* `getCdnCacheInvalidationStatus` - Operazioni obsolete. Questa API è ora deprecata perché l’ API `cdnCacheInvalidation` invalida la cache quasi immediatamente (~5 secondi). Di conseguenza, non è più necessario eseguire il polling per lo stato di invalidazione.
