---
description: Restituisce informazioni sulla struttura di una società (numero di file, ecc.).
seo-description: Restituisce informazioni sulla struttura di una società (numero di file, ecc.).
seo-title: getDiskUsage
solution: Experience Manager
title: getDiskUsage
topic: Scene7 Image Production System API
uuid: 29190200-8f49-4689-9782-1df665dca1b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 11%

---


# getDiskUsage{#getdiskusage}

Restituisce informazioni sulla struttura di una società (numero di file, ecc.).

## Tipi di utenti autorizzati {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Input (getDiskUsageParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società di cui si desidera ottenere l’utilizzo del disco. |

**Output (getDiskUsageReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`diskUsageArray`*` | `types:DiskUsageArray` | Sì | Array di utilizzo del disco aziendale. |

## Esempi {#section-cb16a97badc94076ad5da277db5ed16a}

Il nome della richiesta è fuorviante. Piuttosto che restituire semplicemente un valore scalare che riflette lo spazio su disco utilizzato da un&#39;azienda, riceve altre informazioni sulla struttura di un&#39;azienda.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**Risposta**

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```

