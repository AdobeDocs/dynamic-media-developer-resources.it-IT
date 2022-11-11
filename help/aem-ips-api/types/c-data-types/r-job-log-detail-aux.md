---
description: Contiene messaggi supplementari associati al messaggio del registro di lavoro principale (JobDetail). Include avvisi e altri dettagli associati alle risorse attualmente elaborate.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

Contiene messaggi supplementari associati al messaggio del registro di lavoro principale (JobDetail). Include avvisi e altri dettagli associati alle risorse attualmente elaborate.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| logMessage | `xsd:string` | Un messaggio ausiliario. |
| logType | `xsd:string` | Tipo di log: `IPSJobLog.gcUploadWarning` o `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | Data di creazione del registro di lavoro ausiliario. |
