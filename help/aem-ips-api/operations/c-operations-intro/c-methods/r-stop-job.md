---
description: Interrompe un processo in corso.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '61'
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
