---
description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 3.8.
seo-description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 3.8.
seo-title: Operazioni nuove e modificate
solution: Experience Manager
title: Operazioni nuove e modificate
topic: Scene7 Image Production System API
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Operazioni: Nuovo e modificato{#operations-new-and-modified}

Descrive i metodi operativi nuovi e modificati per l&#39;API IPS versione 3.8.

Sintassi

## Nuove operazioni {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## Operazioni modificate {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* Il `publishState` parametro opzionale consente di cercare lo stato della `MarkedForPublish/NotMarkedForPublish` risorsa.

**getJobLogs**

* Il `userHandle` parametro opzionale consente di recuperare i registri di processo inviati da un utente specifico.

