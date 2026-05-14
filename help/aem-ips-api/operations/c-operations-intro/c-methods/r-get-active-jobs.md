---
description: Ottiene tutti i processi attualmente attivi.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
TQID: 'https://experienceleague.adobe.com/YTwzh2h9wVPuURKL5nNFoac2SruwYXDw9oWtd-vzowc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
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
