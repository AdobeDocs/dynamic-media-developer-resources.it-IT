---
description: Ottiene tutti i processi attualmente attivi.
seo-description: Ottiene tutti i processi attualmente attivi.
seo-title: getActiveJobs
solution: Experience Manager
title: getActiveJobs
topic: Scene7 Image Production System API
uuid: 3231d349-b254-4dd0-804d-8beaab116b56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 14%

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
| ` *`companyHandle`*` | `xsd:string` | No | L&#39;handle della società. |
| ` *`jobHandle`*` | `xsd:string` | No | L’handle del processo. |
| ` *`OriginalName`*` | `xsd:string` | No | Nome del processo originale. |

**Output (getActiveJobsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`jobArray`*` | `xsd:string` | Sì | Matrice di processi attivi. |

## Esempi {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Questo esempio di codice restituisce tutti i processi attivi di una società in esecuzione in IPS. In questo caso, la risposta è insolita perché il coordinatore della pianificazione IPS è disabilitato senza processi attivi in esecuzione. In circostanze normali, la risposta restituirebbe una serie di posti di lavoro attivi.

**Request Contents (Richiesta contenuto)**

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

