---
description: Ottiene i registri di processo per una risorsa. Gli elementi restituiti nell'array contengono informazioni dettagliate su ciascuna voce nel registro dei processi per tale risorsa. Il campo di risposta logMessage è localizzato in base al campo authHeader.
seo-description: Ottiene i registri di processo per una risorsa. Gli elementi restituiti nell'array contengono informazioni dettagliate su ciascuna voce nel registro dei processi per tale risorsa. Il campo di risposta logMessage è localizzato in base al campo authHeader.
seo-title: getAssetJobLogs
solution: Experience Manager
title: getAssetJobLogs
topic: Dynamic Media Image Production System API
uuid: 7ea81baf-769b-4c73-bbc6-f52c89c98d50
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 7%

---


# getAssetJobLogs{#getassetjoblogs}

Ottiene i registri di processo per una risorsa. Gli elementi restituiti nell&#39;array contengono informazioni dettagliate su ciascuna voce nel registro dei processi per tale risorsa. Il campo di risposta logMessage è localizzato in base al campo authHeader.

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
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle della società alla quale la risorsa appartiene. |
| `*`assetHandle`*` | `xsd:string` | Sì | L’handle della risorsa con i registri di processo da recuperare. |

**Output (getAssetJobLogsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`jobLogArray`*` | `types:AssetJobLogArray` | Sì | Matrice registro processi. |

## Esempi {#section-f03d7f3ec5d043d38227f926fb7609f6}

Questo esempio di codice recupera i registri di processo di una risorsa specifica. La risposta restituisce un array di registri di processo con informazioni dettagliate su tutti i processi in cui è stata utilizzata la risorsa.

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

