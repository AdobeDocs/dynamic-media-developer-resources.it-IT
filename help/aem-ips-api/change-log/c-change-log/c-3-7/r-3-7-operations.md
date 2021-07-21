---
description: Descrive i metodi operativi nuovi e modificati per l’API IPS versione 3.7.
solution: Experience Manager
title: Operazioni nuove e modificate
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
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
