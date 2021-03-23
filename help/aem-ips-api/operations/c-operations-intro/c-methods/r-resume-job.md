---
description: Riavvia un lavoro in pausa.
seo-description: Riavvia un lavoro in pausa.
seo-title: curriculumJob
solution: Experience Manager
title: curriculumJob
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 12%

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
