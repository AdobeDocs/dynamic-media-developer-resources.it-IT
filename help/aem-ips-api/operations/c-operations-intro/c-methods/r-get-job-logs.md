---
description: Ottiene i registri di lavoro specificati per la società selezionata. Puoi ordinare in base a caratteri, direzione, date di inizio e fine e numero di righe.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 9%

---


# getJobLogs{#getjoblogs}

Ottiene i registri di lavoro specificati per la società selezionata. Puoi ordinare in base a caratteri, direzione, date di inizio e fine e numero di righe.

Sintassi

## Tipi di utenti autorizzati {#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-8cfdc7994da24678a45edcb37e9a2166}

**Input (getJobLogsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | No | L&#39;azienda gestisce. |
| `*`userHandle`*` | `xsd:string` | No | Ottiene i registri dei processi inviati da un utente specifico. |
| `*`sortBy`*` | `xsd:string` | No | Consente di selezionare i campi di ordinamento. |
| `*`sortDirection`*` | `xsd:string` | No | Ordinamento (crescente o decrescente). |
| `*`startDate`*` | `xsd:dateTime` | No | Data e ora dell&#39;inizio del job log. Specifica il fuso orario con la richiesta per questo campo. |
| `*`endDate`*` | `xsd:dateTime` | No | Data e ora della fine del job log. Specifica il fuso orario con la richiesta per questo campo. |
| `*`numRows`*` | `xsd:int` | No | Numero massimo di righe da restituire. |

**Output (getJobLogsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`jobLogArray`*` | `types: JobLogArray` | Sì | Array di registri di lavoro. |

## Esempi {#section-35871c94b4a44559912577efddbc46a6}

Questo esempio di codice restituisce i registri di lavoro IPS per una società specifica. Puoi anche utilizzarlo per restituire i registri di lavoro di un utente specifico, di un&#39;azienda o di un utente specifico.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**Risposta**

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```

