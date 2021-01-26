---
description: Descrive i metodi operativi nuovi e modificati per l'API IPS versione 3.7.
solution: Experience Manager
title: Operazioni nuove e modificate
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '48'
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

