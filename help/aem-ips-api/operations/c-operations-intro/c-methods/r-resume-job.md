---
description: Riavvia un lavoro in pausa.
solution: Experience Manager
title: curriculumJob
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 13%

---

# curriculumJob{#resumejob}

Riavvia un lavoro in pausa.

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
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle dell&#39;azienda con il processo che si desidera riavviare. |
| `*`jobHandle`*` | `xsd:string` | Sì | Maniglia del processo sospeso. |

**Output (curriculumJobReturn)**

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
