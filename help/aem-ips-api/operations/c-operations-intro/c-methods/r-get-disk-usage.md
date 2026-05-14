---
description: Restituisce informazioni sulla struttura di un'azienda (numero di file e così via).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
TQID: 'https://experienceleague.adobe.com/mF0YHIw8BZhBRK240EmiiaHoyBbTdaW-ajl7veY1ywk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 9%

---

# getDiskUsage{#getdiskusage}

Restituisce informazioni sulla struttura di un&#39;azienda (numero di file e così via).

## Tipi di utenti autorizzati {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Input (getDiskUsageParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle per l&#39;azienda di cui si desidera ottenere l&#39;utilizzo del disco. |

**Output (getDiskUsageReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| diskUsageArray | `types:DiskUsageArray` | Sì | Array di utilizzo del disco aziendale. |

## Esempi {#section-cb16a97badc94076ad5da277db5ed16a}

Il nome di questa richiesta è fuorviante. Anziché restituire semplicemente un valore scalare che rifletta la quantità di spazio su disco utilizzata da un&#39;azienda, questa ottiene anche altre informazioni sulla struttura di un&#39;azienda.

**Richiesta**

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
