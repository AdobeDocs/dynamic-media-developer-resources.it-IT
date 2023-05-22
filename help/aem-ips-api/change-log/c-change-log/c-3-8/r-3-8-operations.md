---
description: Descrive i metodi operativi nuovi e modificati per la versione 3.8 dell'API IPS.
solution: Experience Manager
title: Operazioni nuove e modificate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# Operazioni: nuove e modificate{#operations-new-and-modified}

Descrive i metodi operativi nuovi e modificati per la versione 3.8 dell&#39;API IPS.

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

* L&#39;opzione `publishState` consente di eseguire ricerche nel `MarkedForPublish/NotMarkedForPublish` stato risorsa.

**getJobLogs**

* L&#39;opzione `userHandle` Il parametro consente di recuperare i registri di processo inviati da un utente specifico.
