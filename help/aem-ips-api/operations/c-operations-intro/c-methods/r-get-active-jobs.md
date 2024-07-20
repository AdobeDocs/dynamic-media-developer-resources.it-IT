---
description: Ottiene tutti i processi attualmente attivi.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 11%

---

# getActiveJobs{#getactivejobs}

Ottiene tutti i processi attualmente attivi.

Sintassi

## Tipi di utenti autorizzati {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**Input (getActiveJobsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | No | La maniglia per l&#39;azienda. |
| jobHandle | `xsd:string` | No | Handle del processo. |
| originalName | `xsd:string` | No | Nome processo originale. |

**Output (getActiveJobsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| jobArray | `xsd:string` | Sì | Array di processi attivi. |

## Esempi {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

In questo esempio di codice vengono restituiti tutti i processi attivi di una società in esecuzione in IPS. In questo caso, la risposta è insolita perché il coordinatore della pianificazione IPS è disabilitato senza processi attivi in esecuzione. In circostanze normali, la risposta restituirebbe un certo numero di posti di lavoro attivi.

**Richiesta**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**Risposta**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```
