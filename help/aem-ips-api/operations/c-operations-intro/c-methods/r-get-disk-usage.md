---
description: Restituisce informazioni sulla struttura di un'azienda (numero di file, ecc.).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 12%

---


# getDiskUsage{#getdiskusage}

Restituisce informazioni sulla struttura di un&#39;azienda (numero di file, ecc.).

## Tipi di utenti autorizzati {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Input (getDiskUsageParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle dell&#39;azienda di cui si desidera ottenere l&#39;utilizzo del disco. |

**Output (getDiskUsageReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`diskUsageArray`*` | `types:DiskUsageArray` | Sì | Array di utilizzo del disco aziendale. |

## Esempi {#section-cb16a97badc94076ad5da277db5ed16a}

Il nome della richiesta è fuorviante. Invece di restituire semplicemente un valore scalare che riflette lo spazio su disco utilizzato da un&#39;azienda, ottiene altre informazioni anche sulla struttura di un&#39;azienda.

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

