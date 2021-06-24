---
description: Descrive i metodi operativi nuovi e modificati per l’API IPS versione 3.7.
solution: Experience Manager
title: Operazioni nuove e modificate
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '53'
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
