---
description: Interrompe un processo in corso.
seo-description: Interrompe un processo in corso.
seo-title: stopJob
solution: Experience Manager
title: stopJob
topic: Scene7 Image Production System API
uuid: 698c1652-5afa-4a2c-819a-1ba6ffc6aacf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 16%

---


# stopJob{#stopjob}

Interrompe un processo in corso.

Sintassi

## Tipi di utenti autorizzati {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-2b64f074e37c4c38849994f3bc65342a}

**Input (stopJobParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | Maniglia aziendale. |
| ` *`jobHandle`*` | `xsd:string` | Sì | Gestite il lavoro che desiderate interrompere. |

**Output (stopJobReturn0**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-f7e07fa09ae24dc89685533f20ab3b81}

**Request Contents (Richiesta contenuto)**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**Risposta**

Nessuno.
