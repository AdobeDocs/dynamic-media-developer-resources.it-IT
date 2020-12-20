---
description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 3.7.
seo-description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 3.7.
seo-title: Operazioni nuove e modificate
solution: Experience Manager
title: Operazioni nuove e modificate
topic: Scene7 Image Production System API
uuid: 3c163157-cd0d-4887-a1f0-7941d96c36f9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---


# Operazioni: Nuovo e modificato{#operations-new-and-modified}

Descrive i metodi operativi nuovi e modificati per l&#39;API IPS versione 3.7.

Sintassi

## Nuove operazioni {#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset`
* `renameAsset`
* `deleteAsset`
* `createFolder`
* `deleteFolder`
* `getActiveJobs`
* `getScheduledJobs`
* `getJobLogs`
* `getJbLogDetails`
* `submitJob`
* `stopJob`
* `pauseJob`
* `resumeJob`
* `executeJob`
* `deleteJob`

## Operazioni modificate {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* Rimosso il parametro `name`.
* Aggiunto `excludeFieldArray`.

**getFolders**

* Aggiunto `excludeFieldArray`.

**getFolderTree**

* Sono stati aggiunti `excludeFieldArray` e `getUniqueMetadataValues`.
* Realizzato `fieldHandle` come parametro richiesto.

