---
description: Ottiene i registri dei processi per una risorsa. Gli elementi restituiti nella matrice contengono informazioni dettagliate su ogni voce nel registro di lavoro per la risorsa. Il campo di risposta logMessage viene localizzato in base al campo authHeader.
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 8%

---


# getAssetJobLogs{#getassetjoblogs}

Ottiene i registri dei processi per una risorsa. Gli elementi restituiti nella matrice contengono informazioni dettagliate su ogni voce nel registro di lavoro per la risorsa. Il campo di risposta logMessage viene localizzato in base al campo authHeader.

Sintassi

## Tipi di utenti autorizzati {#section-72b98cdb0f6f47f5aabdc183a45ea577}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-9586617e124b4da4acb6b66b2a9adad8}

**Input (getAssetJobLogsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Il handle della società a cui appartiene il cespite. |
| `*`assetHandle`*` | `xsd:string` | Sì | L’handle della risorsa con i registri di lavoro da recuperare. |

**Output (getAssetJobLogsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`jobLogArray`*` | `types:AssetJobLogArray` | Sì | Matrice del registro di lavoro. |

## Esempi {#section-f03d7f3ec5d043d38227f926fb7609f6}

Questo esempio di codice recupera i registri di lavoro di una risorsa specifica. La risposta restituisce una matrice del registro di lavoro con informazioni dettagliate su tutti i processi in cui è stata utilizzata la risorsa.

**Request Contents (Richiesta contenuto)**

```java
<getAssetJobLogsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetJobLogsParam>
```

**Risposta**

```java
<getAssetJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <jobLogArray>
      <items>
         <jobHandle>j|6||Add_2007-10-24-16:11:07</jobHandle>
         <jobName>Add_2007-10-24-16:11:07</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS</logMessage>
         <logType>UploadSuccess</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2007-10-24T16:12:32.297-07:00</logDate>
      </items>
      <items>
         <jobHandle>j|6||submitServerUploadJob40_2008-06-11-11:38</jobHandle>
         <jobName>submitServerUploadJob40_2008-06-11-11:38</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS.</logMessage>
         <logType>FileUpdated</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2008-06-11T11:38:48.547-07:00</logDate>
      </items>
   </jobLogArray>
</getAssetJobLogsReturn>
```

