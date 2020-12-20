---
description: Sospende un processo attivo.
seo-description: Sospende un processo attivo.
seo-title: pauseJob
solution: Experience Manager
title: pauseJob
topic: Scene7 Image Production System API
uuid: baad2ad6-46f5-4133-a6d9-8ffadf990a06
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 15%

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
| ` *`companyHandle`*` | `xsd:string` | Sì | Gestite l&#39;azienda. |
| ` *`jobHandle`*` | `xsd:string` | Sì | Passate al processo da mettere in pausa. |

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
