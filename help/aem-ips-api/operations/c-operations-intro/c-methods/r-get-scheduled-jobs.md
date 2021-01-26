---
description: Ottiene i processi pianificati per l'esecuzione.
seo-description: Ottiene i processi pianificati per l'esecuzione.
seo-title: getScheduledJobs
solution: Experience Manager
title: getScheduledJobs
topic: Dynamic Media Image Production System API
uuid: 56b0623b-46d7-4d11-8eea-6543ed364b53
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 18%

---


# getScheduledJobs{#getscheduledjobs}

Ottiene i processi pianificati per l&#39;esecuzione.

Sintassi

## Tipi di utenti autorizzati {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-2af604ff8282460990b9237158187f8f}

**Input (getScheduledJobsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società. |
| `*`jobHandle`*` | `xsd:string` | No | Handle processo. |
| `*`OriginalName`*` | `xsd:string` | No | Nome specificato da `submitJob`. |

**Output (getScheduledJobsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`jobArray`*` | `types:ScheduledJobArray` | Sì | Array di processi pianificati. |

## Esempi {#section-e79e7da86ba848fd9996aa36de462e6c}

Questo esempio di codice restituisce tutti i processi pianificati in un array di processi. La matrice stessa contiene informazioni dettagliate sui processi.

**Request Contents (Richiesta contenuto)**

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**Risposta**

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```

