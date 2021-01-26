---
description: Riavvia un processo in pausa.
seo-description: Riavvia un processo in pausa.
seo-title: curriculumJob
solution: Experience Manager
title: curriculumJob
topic: Dynamic Media Image Production System API
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 13%

---


# curriculumJob{#resumejob}

Riavvia un processo in pausa.

Sintassi

## Tipi di utenti autorizzati {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**Input (curriculumJobParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle della società con il processo da riavviare. |
| `*`jobHandle`*` | `xsd:string` | Sì | handle per il processo in pausa. |

**Output (curriculumRitorno)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-d0524e031f1f43d89430eade19526162}

Questo esempio di codice riavvia un processo in pausa.

**Request Contents (Richiesta contenuto)**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**Risposta**

Nessuno.
