---
description: Sospende un processo attivo.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
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
| `*`companyHandle`*` | `xsd:string` | Sì | Manda all&#39;azienda. |
| `*`jobHandle`*` | `xsd:string` | Sì | Gestisci il processo che desideri mettere in pausa. |

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
