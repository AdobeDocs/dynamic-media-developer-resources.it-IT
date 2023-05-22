---
description: Interrompe un processo in corso.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
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
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| jobHandle | `xsd:string` | Sì | Gestire il processo che si desidera interrompere. |

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
