---
description: Descrive i metodi operativi nuovi e modificati per l’API IPS versione 3.8.
seo-description: Descrive i metodi operativi nuovi e modificati per l’API IPS versione 3.8.
seo-title: Operazioni nuove e modificate
solution: Experience Manager
title: Operazioni nuove e modificate
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---


# Operazioni: Nuovo e modificato{#operations-new-and-modified}

Descrive i metodi operativi nuovi e modificati per l’API IPS versione 3.8.

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

* Il parametro opzionale `publishState` consente di cercare lo stato della risorsa `MarkedForPublish/NotMarkedForPublish`.

**getJobLogs**

* Il parametro opzionale `userHandle` consente di recuperare i registri di lavoro inviati da un utente specifico.

