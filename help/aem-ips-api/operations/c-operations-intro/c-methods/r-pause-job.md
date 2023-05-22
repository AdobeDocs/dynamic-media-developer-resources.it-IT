---
description: Sospende un processo attivo.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 14%

---

# pauseJob{#pausejob}

Sospende un processo attivo.

Sintassi

## Tipi di utenti autorizzati {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-7aedb924cf8b4e05a0dc927636d537a0}

**Input (pauseJobParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Gestire l&#39;azienda. |
| jobHandle | `xsd:string` | Sì | Gestire il processo che si desidera sospendere. |

**Output (PauseJobReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-ee4914f9496f4bd88556728a48fb22c1}

Questo esempio di codice mette in pausa un processo attivo.

**Request Contents (Richiesta contenuto)**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**Risposta**

Nessuno.
