---
description: Contiene messaggi supplementari associati al messaggio del registro di lavoro principale (JobDetail). Include avvisi e altri dettagli associati alle risorse attualmente elaborate.
seo-description: Contiene messaggi supplementari associati al messaggio del registro di lavoro principale (JobDetail). Include avvisi e altri dettagli associati alle risorse attualmente elaborate.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 4%

---


# JobLogDetailAux{#joblogdetailaux}

Contiene messaggi supplementari associati al messaggio del registro di lavoro principale (JobDetail). Include avvisi e altri dettagli associati alle risorse attualmente elaborate.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Un messaggio ausiliario. |
| `*`logType`*` | `xsd:string` | Tipo di log: `IPSJobLog.gcUploadWarning` o `IPSJobLog.gcUploadError`. |
| `*`dateCreated`*` | `xsd:dateTime` | Data di creazione del registro di lavoro ausiliario. |

