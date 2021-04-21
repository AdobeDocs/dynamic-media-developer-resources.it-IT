---
description: Descrive i metodi operativi nuovi e modificati per l’API IPS versione 3.7.
solution: Experience Manager
title: Operazioni nuove e modificate
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---


# Operazioni: Nuovo e modificato{#operations-new-and-modified}

Descrive i metodi operativi nuovi e modificati per l’API IPS versione 3.7.

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

* Parametro `name` rimosso.
* È stato aggiunto `excludeFieldArray`.

**getFolders**

* È stato aggiunto `excludeFieldArray`.

**getFolderTree**

* Sono stati aggiunti `excludeFieldArray` e `getUniqueMetadataValues`.
* È stato impostato `fieldHandle` un parametro obbligatorio.

