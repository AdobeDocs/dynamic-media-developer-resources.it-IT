---
description: Interrompe un processo in corso.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '59'
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
| `*`companyHandle`*` | `xsd:string` | Sì | Tratta l&#39;azienda. |
| `*`jobHandle`*` | `xsd:string` | Sì | Gestisci il lavoro che vuoi interrompere. |

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
