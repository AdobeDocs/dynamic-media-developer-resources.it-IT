---
description: Ottiene i processi pianificati per l'esecuzione.
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
TQID: 'https://experienceleague.adobe.com/DNUaAhcCeO8MvLH5YF5-WTA74fCyRKLxvXBKu0ltngk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 16%

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
| companyHandle | `xsd:string` | Sì | La maniglia per l&#39;azienda. |
| jobHandle | `xsd:string` | No | Handle di processo. |
| originalName | `xsd:string` | No | Il nome specificato da `submitJob`. |

**Output (getScheduledJobsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| jobArray | `types:ScheduledJobArray` | Sì | Array di processi pianificati. |

## Esempi {#section-e79e7da86ba848fd9996aa36de462e6c}

In questo esempio di codice vengono restituiti tutti i processi pianificati in una matrice di processi. L’array stesso contiene informazioni dettagliate sui processi.

**Richiesta**

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
