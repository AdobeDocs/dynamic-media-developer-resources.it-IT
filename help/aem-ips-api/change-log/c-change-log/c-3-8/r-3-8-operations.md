---
description: Descrive i metodi operativi nuovi e modificati per l’API IPS versione 3.8.
solution: Experience Manager
title: Operazioni nuove e modificate
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '67'
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
