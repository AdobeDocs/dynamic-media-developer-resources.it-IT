---
description: Ottiene i registri di processo specificati per la società selezionata. Puoi ordinare in base ai caratteri, alla direzione, alle date di inizio e di fine e al numero di righe.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 8%

---

# getJobLogs{#getjoblogs}

Ottiene i registri di processo specificati per la società selezionata. Puoi ordinare in base ai caratteri, alla direzione, alle date di inizio e di fine e al numero di righe.

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
| companyHandle | `xsd:string` | No | La maniglia aziendale. |
| userHandle | `xsd:string` | No | Ottiene i registri dei processi inviati da un utente specifico. |
| sortBy | `xsd:string` | No | Consente di selezionare i campi di ordinamento. |
| sortDirection | `xsd:string` | No | Ordinamento (crescente o decrescente). |
| startDate | `xsd:dateTime` | No | La data e l’ora di inizio del registro di processo. Fornisci il fuso orario con la richiesta per questo campo. |
| endDate | `xsd:dateTime` | No | La data e l’ora della fine del registro di processo. Fornisci il fuso orario con la richiesta per questo campo. |
| numRows | `xsd:int` | No | Numero massimo di righe da restituire. |

**Output (getJobLogsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| jobLogArray | `types: JobLogArray` | Sì | Array di registri di processo. |

## Esempi {#section-35871c94b4a44559912577efddbc46a6}

In questo esempio di codice vengono restituiti i registri di processo IPS per una società specifica. Puoi utilizzarlo anche per restituire i registri di processo per un utente o un’azienda e un utente specifici.

**Richiesta**

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
