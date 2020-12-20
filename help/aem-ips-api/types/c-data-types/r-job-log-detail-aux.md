---
description: Contiene messaggi aggiuntivi associati al messaggio del registro dei processi principale (JobDetail). Include avvisi e altri dettagli associati alla risorsa attualmente elaborata.
seo-description: Contiene messaggi aggiuntivi associati al messaggio del registro dei processi principale (JobDetail). Include avvisi e altri dettagli associati alla risorsa attualmente elaborata.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
topic: Scene7 Image Production System API
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 4%

---


# JobLogDetailAux{#joblogdetailaux}

Contiene messaggi aggiuntivi associati al messaggio del registro dei processi principale (JobDetail). Include avvisi e altri dettagli associati alla risorsa attualmente elaborata.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`logMessage`*` | `xsd:string` | Un messaggio ausiliario. |
| ` *`logType`*` | `xsd:string` | Tipo di registro: `IPSJobLog.gcUploadWarning` o `IPSJobLog.gcUploadError`. |
| ` *`dateCreate`*` | `xsd:dateTime` | Data di creazione del registro di lavoro ausiliario. |

