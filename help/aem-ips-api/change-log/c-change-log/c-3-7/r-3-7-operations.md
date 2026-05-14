---
description: Descrive i metodi operativi nuovi e modificati per la versione 3.7 dell'API IPS.
solution: Experience Manager
title: Operazioni nuove e modificate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
TQID: 'https://experienceleague.adobe.com/nt-KwoxJw8bSbt076MIIZlXW2YbMzwVURLwE-94hlDU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 50
ht-degree: 0%

---

# Operazioni: nuove e modificate{#operations-new-and-modified}

Descrive i metodi operativi nuovi e modificati per la versione 3.7 dell&#39;API IPS.

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
* Aggiunto `excludeFieldArray`.

**getFolders**

* Aggiunto `excludeFieldArray`.

**getFolderTree**

* Aggiunti `excludeFieldArray` e `getUniqueMetadataValues`.
* `fieldHandle` è un parametro obbligatorio.
