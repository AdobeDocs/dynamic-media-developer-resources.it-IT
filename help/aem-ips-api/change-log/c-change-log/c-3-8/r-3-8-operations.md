---
description: Descrive i metodi operativi nuovi e modificati per l’API IPS versione 3.8.
solution: Experience Manager
title: Operazioni nuove e modificate
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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

